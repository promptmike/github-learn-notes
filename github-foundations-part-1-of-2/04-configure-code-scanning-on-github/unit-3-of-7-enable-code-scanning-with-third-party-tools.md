# Enable code scanning with third party tools

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We can do analysis outside GitHub with third party tools, then upload the results to GitHub
> GitHub supports internal and off-site code scanning

We will learn how to enable third party code scanning and upload Static Analysis Results Interchange Format (SARIF) files
> GitHub supports third party code scanning with the SARIF format

## About SARIF file uploads for code scanning

GitHub creates code-scanning alerts from SARIF 2.1.0 files
> GitHub supports SARIF 2.1.0

Results can be uploaded using the code scanning API, CodeQL CLI or GitHub Actions
> GitHub supports SARIF 2.1.0 upload with API, CodeQL and actions

### Code-scanning API

The code-scanning API can retrieve information from a repository, or from third party tools
> GitHub code-scanning API can retrieve information from multiple sources and automate reporting at the endpoints

`https://api.github.com` sends and receives data in **JSON** format, with support for custom media types
> GitHub API can use multiple sources to send and receive data in JSON format

The code-scanning REST API supports `application/sarif+json`
> The GitHub API sends and receives data in JSON format and code scanning is supported by the `application/sarif+json` custom media format

Using a GET request to the code-scanning REST API with the custom format `application/sarif+json` yields a subset of data for the specific analysis
> GitHub API sends data summaries when using default media type, or specific data subsets when using a custom media format

**Example**
```
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer <YOUR-TOKEN>" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/orgs/ORG/code-scanning/alerts
```
> GitHub API has a default media type, and a custom one specifically for code-scanning

[REST API endpoints for code scanning](https://docs.github.com/en/rest/code-scanning/code-scanning?apiVersion=2022-11-28)

### CodeQL CLI

CodeQL represents code as a database to be queried, and you can even run a suite of queries to generate results in SARIF format for uploading to GitHub
> The GitHub API can directly retrieve code-scanning information, while CodeQL treats code as data, and can therefore be used to generate SARIF files

**CodeQL bundle contents:**
- CodeQL CLI
- A compatible version of the queries and libraries from [codeql](https://github.com/github/codeql)
- Precompiled queries

> The CodeQL bundle contains everything you need to use CodeQL CLI for code-scanning analysis, while the GitHub API supports analysis using HTTPS
[CodeQL bundle download](https://github.com/github/codeql-action/releases)

If you want to use CodeQL, you should always use the bundle to ensure compatibility
> Code scanning results can be uploaded to GitHub using the REST API, or using CodeQL CLI included in the CodeQL bundle

### Code-scanning analysis with GitHub Actions

You can upload third party SARIF to a repo using an Actions workflow YML
> Code scanning results can be uploaded to GitHub using the REST API, CodeQL CLI or an Actions workflow

Your workflow must use the `upload-sarif` action from the `github/codeql-action` repo
> Code scanning results can be uploaded using the API, CodeQL CLI or the `upload-sarif` action in an Actions workflow

The main input parameter is `sarif-file` giving the path to the SARIF files relative to the repo root
> Code scanning results can be uploaded using the API, CodeQL CLI, or an Actions workflow with the `upload-sarif` action and a `sarif-file` path

The `upload-sarif` action can be configured to run on event
> Code scanning results can be uploaded using API, CodeQL CLI, or an Actions workflow trigger

**Example:**
```
name: 'Code Scanning : Upload SARIF'
description: 'Upload the analysis results'
author: 'GitHub'
inputs:
  sarif_file:
    description: |
      The SARIF file or directory of SARIF files to be uploaded to GitHub code scanning.
      See https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/
      uploading-a-sarif-file-to-github#uploading-a-code-scanning-analysis-with-github-actions
      for information on the maximum number of results and maximum file size supported by code scanning.
    required: false
    default: '../results'
  checkout_path:
    description: "The path at which the analyzed repository was checked out. 
    Used to relativize any absolute paths in the uploaded SARIF file."
    required: false
    default: ${{ github.workspace }}
  token:
    default: ${{ github.token }}
  matrix:
    default: ${{ toJson(matrix) }}
  category:
    description: String used by Code Scanning for matching the analyses
    required: false
  wait-for-processing:
    description: If true, the Action will wait for the uploaded SARIF to be processed before completing.
    required: true
    default: "false"
runs:
  using: 'node12'
  main: '../lib/upload-sarif-action.js'
```

GitHub uses properties of the SARIF files to display alerts
> GitHub receives SARIF files by API, CodeQL CLI, or Actions workflows, then uses their properties to display code-scanning alerts

GitHub will attempt to populate empty fields and prevent duplication where possible
> GitHub receives SARIF files, uses their properties to generate alerts and prevent duplication, and attempts to populate empty fields from source files

The maximum results per upload is 5,000
> GitHub can receive up to 5,000 results per upload of SARIF files, using properties to generate alerts and prevent duplications, and attempt to populate empty fields from source

The maximum upload size is 10 MB
> GitHub can receive up to 5,000 results totalling up to 10 MB in a gzip-compressed SARIF file, using its properties to generate alerts and prevent duplication

### Upload SARIF files generated outside your repository

You can create a workflow to upload each SARIF file after you commit it to your repository
> GitHub can receive SARIF files by API, by CodeQL, by Actions workflows triggered on event, or even from Actions workflows triggered by committing the SARIF to repo

This would require a workflow trigger on push, using the `partialFingerprints` property to detect changes
> GitHub can receive SARIF files by API, CodeQL CLI, or Actions workflows using a variety of event triggers

You can set multiple workflow triggers, e.g. on push + scheduled run
> GitHub generates alerts from properties of SARIF files that can be uploaded by API, CodeQL CLI, or Actions workflows runs triggered by events

**Example:**
```
name: "Upload SARIF"

// Run workflow each time code is pushed to your repository and on a schedule. 
//The scheduled workflow runs every Thursday at 15:45 UTC.

on:
  push:
  schedule:
    - cron: '45 15 * * 4'

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      security-events: write
  steps:
    # This step checks out a copy of your repository.
    - name: Checkout repository
      uses: actions/checkout@v2
    - name: Upload SARIF file
      uses: github/codeql-action/upload-sarif@v1
      with:
        # Path to SARIF file relative to the root of the repository
        sarif_file: results.sarif
```

### Upload SARIF files generated as part of a CI workflow

If you generate SARIF files as part of a CI workflow, you can add the `upload-sarif` action as a step after CI tests
> GitHub generates alerts from SARIF files, which you can upload with API, CodeQL CLI, or Actions workflows, and even generate and upload as part of a CI workflow

**Example:**
```
  name: "ESLint analysis"

// Run workflow each time code is pushed to your repository and on a schedule.
// The scheduled workflow runs every Wednesday at 15:45 UTC.
on:
  push:
  schedule:
    - cron: '45 15 * * 3'

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      security-events: write
    steps:
      - uses: actions/checkout@v2
      - name: Run npm install
        run: npm install
      // Runs the ESlint code analysis
      - name: Run ESLint
        // eslint exits 1 if it finds anything to report
        run: node_modules/.bin/eslint build docs lib script spec-main -f node_modules/@microsoft/eslint-formatter-sarif/sarif.js -o results.sarif || true
      // Uploads results.sarif to GitHub repository using the upload-sarif action
      - uses: github/codeql-action/upload-sarif@v1
        with:
          // Path to SARIF file relative to the root of the repository
          sarif_file: results.sarif
  ```

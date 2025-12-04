# Insight and automation with projects

Projects can provide insights and automation
GitHub Projects has tooling for insights and automation

## Insights with Projects

We will learn about the uses of Insights, current and historical charts, and chart customisation
GitHub Projects has tools for current and historical charts, and chart customisation

## Insights and how they can be useful

Charts use project items as source data
Projects has insights and automation, including charts generated from project item data

### Current charts

You can create charts to visualise project items (e.g. issues assigned to each individual, number of issues for each iteration, etc)
Projects offers charts generated from project item data to help you visualise the workflow of your project

You can also filter charts (e.g. only include specific labels or assignees)
Projects offers tools to generate charts from project item data and filter them to extract the information you need

![Current Chart](https://learn.microsoft.com/en-us/training/github/manage-work-github-projects/media/6-current-chart-example.png)

### Historical charts

GitHub Teams and GHEC also offer historical charts to track past trends
Projects can generate current charts from project item data and filter them to extract the information you need, while GitHub Teams and GHEC also have historical charts to track trends

![Historical Chart](https://learn.microsoft.com/en-us/training/github/manage-work-github-projects/media/6-historical-chart-example.png)

### Create and customize charts

**Create Chart**
1. Navigate to project
2. Top-right > Line Graph Button > Hover > *Insights* label
3. Left > *New chart*
4. Filter by keyword or field
5. Right > *Save*

GitHub Projects can generate current charts to visualise item data, and Projects for GitHub Teams and GHEC can also generate historical charts to follow trends

**Customise chart**
1. Left > Select chart
2. Right > *Configure*
3. *Layout* dropdown > Select chart type
4. *X-axis* dropdown > Select field
5. *Group-by* > Select a field, or Select *None* to disable grouping

GitHub Projects can generate charts from item data and allows you to customise them with layouts and field selections to extract the precise insights you need

### Automation with Projects

You can automate using built-in workflows, GraphQL API, or Actions Workflows
GitHub Projects offers customisable charts and multiple ways to automate

Built-in workflows are easiest, while GraphQL and Actions provide more control if needed
GitHub Projects offers customisable charts, built-in workflows for common use cases, and integration with GraphQL and Action in case more fine-tuned automation is needed

### Configure built-in workflows

Built-in workflows help you track all your work in real-time, using triggers to automatically update you
GitHub Projects offers customisable charts and integration with workflows, as well as built-in workflows for common use cases

![Automation Workflows](https://learn.microsoft.com/en-us/training/github/manage-work-github-projects/media/6-automation-workflows-menu.png)
![Default Workflows](https://learn.microsoft.com/en-us/training/github/manage-work-github-projects/media/6-automation-default-workflows-items.png)

1. Top-right > `...` > *Workflows*
2. Left column > *Default workflows* > *Item added to project*
3. Select *Edit* to make changes
4. *When an item is added to the project* > Select both *issues* and *pull requests*
5. *Set Value* section > *Status:Todo*
6. Select *Save and turn on workflow*

GitHub Projects offers customisable charts and built-in workflows, as well as GraphQL and Actions to create your own project workflows

## GitHub Actions with workflows

GitHub Actions allows the highest level of workflow customisation
GitHub Projects has customisable charts, built-in workflows and GraphQL, plus you can make your own workflow from scratch with Actions

For example, **Trigger: Issue Creation** > **Workflow starts** > **Add label** > **Leave comment** > **Move issue to project board**
GitHub Actions can fully configure workflows for projects, but projects also support GraphQL, have built-in workflows and offer customisable charts for project insights

### GraphQL API

If you use GraphQL in GitHub, you can use the API to automate your project
GitHub Projects support Actions and GraphQL workflows, have built-in workflows for common use cases, and offer customisable insight charts derived from items data

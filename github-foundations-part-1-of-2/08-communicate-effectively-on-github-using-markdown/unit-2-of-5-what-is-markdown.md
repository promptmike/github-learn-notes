# What is Markdown?

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

Markdown is a compromise between the power of HTML and the ease of plain text
> GitHub supports Markdown for fast and effective communication

We will learn Markdown and GFM
> GitHub has its own GitHub Flavored Markdown (GFM) syntax

**❗ ==Note==**

This unit is intended to give you a taste of what Markdown is about. For a more in-depth review, reference the Markdown syntax description and GitHub-Flavored Markdown Spec articles.

## Emphasize text

We need to show which parts of the text are highest priority for the reader
> Markdown is a lightweight alternative to HTML for text-based communication with emphasis

*Italic* text is flanked by single asterisk `*` characters or single underscore `_` characters
> Markdown is a lightweight syntax for communication with emphasis, including italics

**Example**
```markdown
This is *italic* text.
This is also _italic_ text.
```
This is *italic* text. This is also _italic_ text.

**Bold** text is flanked by double asterisk `**` or double underscore `__` characters
> Markdown is a lightweight syntax with emphasis formatting, including italics and bold text

**Example**
```markdown
This is **bold** text.
This is also __bold__ text.
```
This is **bold** text. This is also __bold__ text.

You can mix emphases
> Markdown is a lightweight syntax with emphasis formatting, including nestable bold and italic text

**Example**
```markdown
_This is **italic and bold** text_ using a single underscore for italic and double asterisks for bold.
__This is bold and *italic* text__ using double underscores for bold and single asterisks for italic.
```
_This is **italic and bold** text_ using a single underscore for italic and double asterisks for bold.
__This is bold and *italic* text__ using double underscores for bold and single asterisks for italic.

To use an asterisk as a character, precede it with an escape character (in GFM the backslash `\` is the escape)
> Markdown is a lightweight format with italics, bold, and escapes for using the formatting characters as plain text

**Example**
```markdown
\_This is all \*\*plain\*\* text\_.
```
\_This is all \*\*plain\*\* text\_.

## Declare headings

Headings are preceded by a number hash `#` characters equal to the heading's level in the hierarchy (`#` to `######` just like HTML has `<h1>` to `<h6>`)
> Markdown is a lightweight format that supports italics, bold, escapes and a hierarchy of headings

**Example**
```markdown
###### This is H6 text
```
###### This is H6 text

## Link to images and sites

Links have the syntax `[Name](URL)` and images have `![Name](URL)`
> Markdown is a lightweight format that supports italics, bold, escapes, links, images and a hierarchy of headings

**Example**
```markdown
![Link an image.](/learn/azure-devops/shared/media/mara.png)
```
![Link an image.](/learn/azure-devops/shared/media/mara.png)
```markdown
[Link to Microsoft Training](/training)
```
[Link to Microsoft Training](/training)

## Make lists

You can make ordered list items with numbers followed by stops `1.` and unordered list items with dashes `-`
> Markdown supports italics, bold, escapes, links, images, headings, ordered lists and unordered lists with a lighter syntax than HTML

**Example**
```markdown
1. First
1. Second
1. Third
```
1. First
1. Second
1. Third
```markdown
- First
  - Nested
- Second
- Third
```

## Build tables

Tables use pipes `|` for columns and dashes `-` to designate the previous row as a header
> Markdown supports italics, bold, escapes, links, images, headers, ordered lists, unordered lists and tables with a lighter syntax than HTML

**Example**
```markdown
First|Second
-|-
1|2
3|4
```
First|Second
-|-
1|2
3|4

## Quote text

Blockquotes are preceded by the `>` character
> Markdown supports italics, bold, excapes, links, images, headers, ordered lists, unordered lists, tables and quotes with a lighter syntax than HTML

**Example**
```markdown
> This is quoted text.
```
> This is quoted text.

## Fill the gaps with inline HTML

You can use HTML inline for everything not supported by Markdown
> Markdown offers the most commonly used HTML formatting in a lighter syntax, and supports inline HTML for everything else

**Example**
```markdown
Here is a<br />line break
```
Here is a<br />line break

## Work with code

Code is wrapped in backticks
> Markdown offers common HTML formatting and code blocks, with support for inline HTML to fill the gaps

**Example**
```markdown
This is `code`.
```
This is `code`.

Fenced code blocks are wrapped in triple backticks
> Markdown offers a light syntax for code blocks and most HTML formatting, and also supports inline HTML

**Example**
```markdown
```markdown
var first = 1;
var second = 2;
var sum = first + second;
```
```

```markdown
var first = 1;
var second = 2;
var sum = first + second;
```

GFM adds language specification to Markdown - you can just type the language after the first set of backticks
> Markdown offers light syntax for HTML formatting, and GFM extends this with extra features


**Example**
```markdown
```javascript
var first = 1;
var second = 2;
var sum = first + second;
```
```

```javascript
var first = 1;
var second = 2;
var sum = first + second;
```

## Cross-link issues and pull requests

GFM supports shortcodes `#ID` to link to issues and pull requests, and automatically shortens longer links
> Markdown offers a lightweight syntax for HTML formatting, and GFM extends this to further help with code collaboration

**Example**

| Reference Type | Raw Reference | Short Link |
| -------------- | ------------- | ---------- |
| Issue or pull request URL | `https://github.com/desktop/desktop/pull/3602` | `#3602` |
| `#` and issue or pull request number | `#3602` | `#3602` |
| `GH-` and issue or pull request number | `GH-3602` | `GH-3602` |
| `Username/Repository#` and issue or pull request number | `desktop/desktop#3602` | `deskktop/desktop#3602` |

## Link specific commits

You can link to a commit with its *ID* or **SHA hash**
> Markdown offers a lightweight syntax for HTML formatting, and GFM extends this with additional features such as language specification and GitHub item links

**Example**

| Reference Type | Raw Reference | Short Link |
| -------------- | ------------- | ---------- |
| Commit URL | `https://github.com/desktop/desktop/commit/` |  |
| `8304e9c271a5e5ab4fda797304cd7bcca7158c87` | `8304e9c` | |
| SHA | 8304e9c271a5e5ab4fda797304cd7bcca7158c87 | 8304e9c |
| User@SHA | desktop@8304e9c271a5e5ab4fda797304cd7bcca7158c87 | desktop@8304e9c |
| Username/Repository@SHA | desktop/desktop@8304e9c271a5e5ab4fda797304cd7bcca7158c87 | desktop/desktop@8304e9c |

## Mention users and teams

To highlight a user or team, make an @mention with an `@` character before the name
> Markdown is a lightweight alternative to HTML, while GFM extends it with language specification, item links and @mentions

**Example**
```markdown
@githubteacher
```
@githubteacher

## Track task lists

Use task list items in issues and pull requests using `- [x]` to help track progress or even create sub-issues later
> Markdown is a lightweight alternative to HTML, while GFM extends it with language specification, item links, @mentions and task lists in items

```markdown
- [x] First task
- [x] Second task
- [ ] Third task
```
![Task List](https://learn.microsoft.com/en-us/training/github/communicate-using-markdown/media/2-task-list.png)

## Slash commands

Slash commands are a shorthand for GFM to save time typing
> Markdown is a lightweight alternative to HTML syntax, while GFM extends it with language specification, item links, @mentions, task lists, and slash commands

You can use slash commands in descriptions and comment fields in issues, pull requests, or discussions where supported
> Markdown is a lightweight alternative to HTML syntax, while GFM extends it with language specification, item links, @mentions, task lists and slash commands for easier collaboration

| Command | Description |
| ------- | ----------- |
| `/code` | Code block with your choice of language |
| `/details` | Collapsible detail area |
| `/saved-replies` | Insert saved reply from your account. Use `%cursor%` to place the cursor. |
| `/table` | Table with your choice of columns and rows |
| `/tasklist` | Insert tasklist in *issue description* |
| `/template` | Choose a template to insert |

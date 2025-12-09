# scholar_md

Scholar md is a simple CLI tool for converting md documents to docx (Word) files based on GOST standards.

## Idea

The main benefit of scholar_md is a comfort editing of code and text together in md files,
simple text writing and another features which you can get using markdown syntax.


## Configuration

Of course, each document has unqiue settings like a special fonts, text setups, footnotes, fields, etc.
to respond on this requirements we using one configuration file which describes naming, including and special configs.

TOML file examples:

```toml
[project]
name = "Project Name"

[markdown]
meta_mark = "%"
index_file = "index.md"

[page]
# [<top>, <right>, <bottom>, <left>]
margins = [25, 20, 25, 30]

[fonts]
# [<font name>, <font size>]
base = ["Times New Roman", 14]
code = ["Consolas", 14]
footnote = ["Times New Roman", 12]
```


## Syntax

```md
First paragraph..
% include("parts/1.md")

Second paragraph.

* First option
* Second option
* Third option

% break()

First paragraph on second page. Code example:
\`\`\`python
print("Hello, World!")
\`\`\`

```

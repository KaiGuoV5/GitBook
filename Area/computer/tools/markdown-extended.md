---
description: Markdown extended
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# 🖊 Markdown Extended

## 1 Overview

The [markdown-basic.md](markdown-basic.md "mention") outlined in the original Markdown design document added many of the elements needed on a day-to-day basis, but it wasn’t enough for some people. That’s where extended syntax comes in.

Several individuals and organizations took it upon themselves to extend the basic syntax by adding additional elements like tables, code blocks, syntax highlighting, URL auto-linking, and footnotes. These elements can be enabled by using a lightweight markup language that builds upon the basic Markdown syntax, or by adding an extension to a compatible Markdown processor.

## 2 Availability

Not all Markdown applications support extended syntax elements. You’ll need to check whether or not the lightweight markup language your application is using supports the extended syntax elements you want to use. If it doesn’t, it may still be possible to enable extensions in your Markdown processor.

### Lightweight Markup Languages

There are several lightweight markup languages that are _supersets_ of Markdown. They include basic syntax and build upon it by adding additional elements like tables, code blocks, syntax highlighting, URL auto-linking, and footnotes. Many of the most popular Markdown applications use one of the following lightweight markup languages:

* [CommonMark](https://commonmark.org)
* [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/)
* [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/)
* [MultiMarkdown](https://fletcherpenney.net/multimarkdown/)
* [R Markdown](https://rmarkdown.rstudio.com/)

### Markdown Processors

There are [dozens of Markdown processors](https://github.com/markdown/markdown.github.com/wiki/Implementations) available. Many of them allow you to add extensions that enable extended syntax elements. Check your processor’s documentation for more information.

## 3 Tables

To add a table, use three or more hyphens (`---`) to create each column’s header, and use pipes (`|`) to separate each column. For compatibility, you should also add a pipe on either end of the row.

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        | 
```

The rendered output looks like this:

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

Cell widths can vary, as shown below. The rendered output will look the same.

```
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text | 
```

> 💡 **Tip:** Creating tables with hyphens and pipes can be tedious. To speed up the process, try using the [Markdown Tables Generator](https://www.tablesgenerator.com/markdown\_tables) or [AnyWayData Markdown Export](https://anywaydata.com). Build a table using the graphical interface, and then copy the generated Markdown-formatted text into your file.

### Alignment

You can align text in the columns to the left, right, or center by adding a colon (`:`) to the left, right, or on both side of the hyphens within the header row.

```
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      | 
```

The rendered output looks like this:

| Syntax    | Description |   Test Text |
| --------- | :---------: | ----------: |
| Header    |    Title    | Here’s this |
| Paragraph |     Text    |    And more |

### Formatting Text in Tables

You can format the text within tables. For example, you can add links, code (words or phrases in backticks (`` ` ``) only, not code blocks), and emphasis.

You can’t use headings, blockquotes, lists, horizontal rules, images, or most HTML tags.

> 💡 **Tip:** You can use HTML to create line breaks and add lists within table cells.

### Escaping Pipe Characters in Tables

You can display a pipe (`|`) character in a table by using its HTML character code (`&#124;`).

## 4 Fenced Code Blocks

The basic Markdown syntax allows you to create code blocks by indenting lines by four spaces or one tab. If you find that inconvenient, try using fenced code blocks. Depending on your Markdown processor or editor, you’ll use three backticks (` ``` `) or three tildes (`~~~`) on the lines before and after the code block. The best part? You don’t have to indent any lines!

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

The rendered output looks like this:

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
} 
```

> 💡 **Tip:** Need to display backticks inside a code block? See \[\[MarkdownBasic#Escaping Backticks|this section]] to learn how to escape them.

#### Syntax Highlighting

Many Markdown processors support syntax highlighting for fenced code blocks. This feature allows you to add color highlighting for whatever language your code was written in. To add syntax highlighting, specify a language next to the backticks before the fenced code block.

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

The rendered output looks like this:

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## 5 Footnotes

Footnotes allow you to add notes and references without cluttering the body of the document. When you create a footnote, a superscript number with a link appears where you added the footnote reference. Readers can click the link to jump to the content of the footnote at the bottom of the page.

To create a footnote reference, add a caret and an identifier inside brackets (`[^1]`). Identifiers can be numbers or words, but they can’t contain spaces or tabs. Identifiers only correlate the footnote reference with the footnote itself — in the output, footnotes are numbered sequentially.

Add the footnote using another caret and number inside brackets with a colon and text (`[^1]: My footnote.`). You don’t have to put footnotes at the end of the document. You can put them anywhere except inside other elements like lists, block quotes, and tables.

```
Here's a simple footnote,[^1] and here's a longer one.[^bignote]


[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.
    
    `{ my code }`
    
    Add as many paragraphs as you like. 
```

The rendered output looks like this:

Here’s a simple footnote,1 and here’s a longer one.2

1. This is the first footnote. ↩
2.  Here’s one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like. ↩

## 6 Heading IDs

Many Markdown processors support custom IDs for \[\[MarkdownBasic#Headings|headings]] — some Markdown processors automatically add them. Adding custom IDs allows you to link directly to headings and modify them with CSS. To add a custom heading ID, enclose the custom ID in curly braces on the same line as the heading.

```
### My Great Heading {#custom-id} 
```

The HTML looks like this:

```
<h3 id="custom-id">My Great Heading</h3> 
```

### Linking to Heading IDs

You can link to headings with custom IDs in the file by creating a \[\[MarkdownBasic#Links|standard link]] with a number sign (`#`) followed by the custom heading ID. These are commonly referred to as _anchor links_.

| Markdown                      | HTML                                     | Rendered Output |
| ----------------------------- | ---------------------------------------- | --------------- |
| `[Heading IDs](#heading-ids)` | `<a href="#heading-ids">Heading IDs</a>` | Heading IDs     |

Other websites can link to the heading by adding the custom heading ID to the full URL of the webpage (e.g, `[Heading IDs](https://www.markdownguide.org/extended-syntax#heading-ids)`).

## 8 Definition Lists

Some Markdown processors allow you to create _definition lists_ of terms and their corresponding definitions. To create a definition list, type the term on the first line. On the next line, type a colon followed by a space and the definition.

```
First Term
: This is the definition of the first term.


Second Term
: This is one definition of the second term.
: This is another definition of the second term. 
```

The HTML looks like this:

```html
<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl> 
```

The rendered output looks like this:

**First Term**

This is the definition of the first term.

**Second Term**

This is one definition of the second term.

This is another definition of the second term.

## 9 Strikethrough

You can strikethrough words by putting a horizontal line through the center of them. The result looks ~~like this~~. This feature allows you to indicate that certain words are a mistake not meant for inclusion in the document. To strikethrough words, use two tilde symbols (`~~`) before and after the words.

```
~~The world is flat.~~ We now know that the world is round. 
```

The rendered output looks like this:

~~The world is flat.~~ We now know that the world is round.

## 10 Task Lists

Task lists (also referred to as _checklists_ and _todo_ lists) allow you to create a list of items with checkboxes. In Markdown applications that support task lists, checkboxes will be displayed next to the content. To create a task list, add dashes (`-`) and brackets with a space (`[ ]`) in front of task list items. To select a checkbox, add an `x` in between the brackets (`[x]`).

```
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media 
```

The rendered output looks like this:

<div align="left">

<img src="https://d33wubrfki0l68.cloudfront.net/54914727add678921954b094b9cca57f63bd6e2e/666d3/assets/images/tasklist.png" alt="Markdown task list">

</div>

## 11 Emoji

There are two ways to add emoji to Markdown files: copy and paste the emoji into your Markdown-formatted text, or type _emoji shortcodes_.

### Copying and Pasting Emoji

In most cases, you can simply copy an emoji from a source like [Emojipedia](https://emojipedia.org/) and paste it into your document. Many Markdown applications will automatically display the emoji in the Markdown-formatted text. The HTML and PDF files you export from your Markdown application should display the emoji.

> 💡 **Tip:** If you're using a static site generator, make sure you [encode HTML pages as UTF-8](https://www.w3.org/International/tutorials/tutorial-char-enc/).

### Using Emoji Shortcodes

Some Markdown applications allow you to insert emoji by typing emoji shortcodes. These begin and end with a colon and include the name of an emoji.

```
Gone camping! :tent: Be back soon.


That is so funny! :joy: 
```

The rendered output looks like this:

Gone camping! ⛺ Be back soon.

That is so funny! 😂

> 📝 **Note:** You can use this [list of emoji shortcodes](https://gist.github.com/rxaviers/7360908), but keep in mind that emoji shortcodes vary from application to application. Refer to your Markdown application's documentation for more information.

## 12 Highlight

This isn’t common, but some Markdown processors allow you to highlight text. The result looks like this. To highlight words, use two equal signs (`==`) before and after the words.

```
I need to highlight these ==very important words==. 
```

The rendered output looks like this:

I need to highlight these ==very important words==.

Alternatively, if your Markdown application supports \[\[MarkdownBasic#HTML|HTML]], you can use the `mark` HTML tag.

```html
I need to highlight these <mark>very important words</mark>. 
```

## 13 Subscript

This isn’t common, but some Markdown processors allow you to use _subscript_ to position one or more characters slightly below the normal line of type. To create a subscript, use one tilde symbol (`~`) before and after the characters.

```
H~2~O
```

The rendered output looks like this:

H2O

> 💡 **Tip:** Be sure to test this in your Markdown application before using it. Some Markdown applications use one tilde symbol before and after words not for subscript, but for strikethrough.

Alternatively, if your Markdown application supports \[\[MarkdownBasic#HTML|HTML]], you can use the `sub` HTML tag.

```
H<sub>2</sub>O 
```

## 14 Superscript

This isn’t common, but some Markdown processors allow you to use _superscript_ to position one or more characters slightly above the normal line of type. To create a superscript, use one caret symbol (`^`) before and after the characters.

```
X^2^ 
```

The rendered output looks like this:

X2

Alternatively, if your Markdown application supports \[\[MarkdownBasic#HTML|HTML]], you can use the `sup` HTML tag.

```
X<sup>2</sup> 
```

## 15 Automatic URL Linking

Many Markdown processors automatically turn URLs into links. That means if you type http://www.example.com, your Markdown processor will automatically turn it into a link even though you haven’t used brackets.

```
http://www.example.com 
```

The rendered output looks like this:

[http://www.example.com](http://www.example.com)

## 16 Disabling Automatic URL Linking

If you don’t want a URL to be automatically linked, you can remove the link by denoting the URL as code with backticks.

```
`http://www.example.com` 
```

The rendered output looks like this:

`http://www.example.com`

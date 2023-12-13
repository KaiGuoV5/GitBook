---
description: Markdown basic syntax
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

# 🖊 Markdown Basic

## 1 Overview

Nearly all Markdown applications support the basic syntax outlined in the original Markdown design document. There are minor variations and discrepancies between Markdown processors — those are noted inline wherever possible.

We can edit online [Markdown Online](https://markdown.com.cn/editor/)。

## 2 Headings

To create a heading, add number signs (#) in front of a word or phrase. The number of number signs you use should correspond to the heading level. For example, to create a heading level three (`<h3>`), use three number signs (e.g., `### My Header`).

<table><thead><tr><th width="289">Markdown</th><th width="277">HTML</th><th>Rendered Output</th></tr></thead><tbody><tr><td><code># Heading level 1</code></td><td><code>&#x3C;h1>Heading level 1&#x3C;/h1></code></td><td><h2>Heading level 1</h2></td></tr><tr><td><code>## Heading level 2</code></td><td><code>&#x3C;h2>Heading level 2&#x3C;/h2></code></td><td><h3>Heading level 2</h3></td></tr><tr><td><code>### Heading level 3</code></td><td><code>&#x3C;h3>Heading level 3&#x3C;/h3></code></td><td><h4>Heading level 3</h4></td></tr><tr><td><code>#### Heading level 4</code></td><td><code>&#x3C;h4>Heading level 4&#x3C;/h4></code></td><td><strong>Heading level 4</strong></td></tr><tr><td><code>##### Heading level 5</code></td><td><code>&#x3C;h5>Heading level 5&#x3C;/h5></code></td><td><strong>Heading level 5</strong></td></tr><tr><td><code>###### Heading level 6</code></td><td><code>&#x3C;h6>Heading level 6&#x3C;/h6></code></td><td><strong>Heading level 6</strong></td></tr></tbody></table>

### Alternate Syntax

Alternatively, on the line below the text, add any number of == characters for heading level 1 or -- characters for heading level 2.

| Markdown                                  | HTML                       | Rendered Output          |
| ----------------------------------------- | -------------------------- | ------------------------ |
| <p>Heading level 1<br>===============</p> | `<h1>Heading level 1</h1>` | <h2>Heading level 1</h2> |
| <p>Heading level 2<br>---------------</p> | `<h2>Heading level 2</h2>` | <h3>Heading level 2</h3> |

> Heading Best Practices

Markdown applications don’t agree on how to handle a missing space between the number signs (#) and the heading name. For compatibility, always put a space between the number signs and the heading name.

| ✅ Do this            | ❌ Don't do this     |
| -------------------- | ------------------- |
| `# Here's a Heading` | `#Here's a Heading` |

You should also put blank lines before and after a heading for compatibility.

| ✅ Do this                                                                                             | ❌ Don't do this                                                                                    |
| ----------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| <p>Try to put a blank line before...<br><br><code># Heading</code><br><br>...and after a heading.</p> | <p>Without blank lines, this might not look right.<br><code># Heading</code><br>Don't do this!</p> |

## 3 Paragraphs

To create paragraphs, use a blank line to separate one or more lines of text.

| Markdown                                                                                                   | HTML                                                                                                                                                                   | Rendered Output                                                                                           |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| <p>I really like using Markdown.<br><br>I think I'll use it to format all of my documents from now on.</p> | <p><code>&#x3C;p>I really like using Markdown.&#x3C;/p></code><br><br><code>&#x3C;p>I think I'll use it to format all of my documents from now on.&#x3C;/p></code></p> | <p>I really like using Markdown.</p><p>I think I'll use it to format all of my documents from now on.</p> |

> Paragraph Best Practices

Unless the [paragraph is in a list](app://obsidian.md/MarkdownBasic#Adding%20Elements%20in%20Lists#Paragraphs), don’t indent paragraphs with spaces or tabs.

> 📝 **Note:** If you need to indent paragraphs in the output, see the [section](app://obsidian.md/MarkdownAdvance#Indent%20\(Tab\)) on how to indent (tab).

| ✅ Do this                                                                                              | ❌ Don't do this                                                                                                           |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| <p>Don't put tabs or spaces in front of your paragraphs.<br><br>Keep lines left-aligned like this.</p> | <p>    This can result in unexpected formatting problems.<br><br>    Don't add tabs or spaces in front of paragraphs.</p> |

## 4 Line Breaks

To create a line break or new line (`<br>`), end a line with two or more spaces, and then type return.

| Markdown                                                       | HTML                                                                                                               | Rendered Output                                                |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------- |
| <p>This is the first line.<br>And this is the second line.</p> | <p><code>&#x3C;p>This is the first line.&#x3C;br></code><br><code>And this is the second line.&#x3C;/p></code></p> | <p>This is the first line.<br>And this is the second line.</p> |

> Line Break Best Practices

You can use two or more spaces (commonly referred to as “trailing whitespace”) for line breaks in nearly every Markdown application, but it’s controversial. It’s hard to see trailing whitespace in an editor, and many people accidentally or intentionally put two spaces after every sentence. For this reason, you may want to use something other than trailing whitespace for line breaks. If your Markdown application [supports HTML](app://obsidian.md/index.html#HTML), you can use the `<br>` HTML tag.

For compatibility, use trailing white space or the `<br>` HTML tag at the end of the line.

There are two other options I don’t recommend using. CommonMark and a few other lightweight markup languages let you type a backslash (`\`) at the end of the line, but not all Markdown applications support this, so it isn’t a great option from a compatibility perspective. And at least a couple lightweight markup languages don’t require anything at the end of the line — just type `return` and they’ll create a line break.

| ✅ Do this                                                                                                                                                | ❌ Don't do this                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| <p>First line with two spaces after.   <br>And the next line.<br><br>First line with the HTML tag after.<code>&#x3C;br></code><br>And the next line.</p> | <p>First line with a backslash after.\<br>And the next line.<br><br>First line with nothing after.<br>And the next line.</p> |

## 5 Emphasis

You can add emphasis by making text bold or italic.

### Bold

To bold text, add two asterisks or underscores before and after a word or phrase. To bold the middle of a word for emphasis, add two asterisks without spaces around the letters.

| Markdown                     | HTML                                      | Rendered Output            |
| ---------------------------- | ----------------------------------------- | -------------------------- |
| `I just love **bold text**.` | `I just love <strong>bold text</strong>.` | I just love **bold text**. |
| `I just love __bold text__.` | `I just love <strong>bold text</strong>.` | I just love **bold text**. |
| `Love**is**bold`             | `Love<strong>is</strong>bold`             | Love**is**bold             |

#### Bold Best Practices

Markdown applications don’t agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to bold the middle of a word for emphasis.

| ✅ Do this        | ❌ Don't do this  |
| ---------------- | ---------------- |
| `Love**is**bold` | `Love__is__bold` |

### Italic

To italicize text, add one asterisk or underscore before and after a word or phrase. To italicize the middle of a word for emphasis, add one asterisk without spaces around the letters.

| Markdown                               | HTML                                          | Rendered Output                      |
| -------------------------------------- | --------------------------------------------- | ------------------------------------ |
| `Italicized text is the *cat's meow*.` | `Italicized text is the <em>cat's meow</em>.` | Italicized text is the _cat’s meow_. |
| `Italicized text is the _cat's meow_.` | `Italicized text is the <em>cat's meow</em>.` | Italicized text is the _cat’s meow_. |
| `A*cat*meow`                           | `A<em>cat</em>meow`                           | A_cat_meow                           |

#### Italic Best Practices

Markdown applications don’t agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to italicize the middle of a word for emphasis.

| ✅ Do this    | ❌ Don't do this |
| ------------ | --------------- |
| `A*cat*meow` | `A_cat_meow`    |

### Bold and Italic

To emphasize text with bold and italics at the same time, add three asterisks or underscores before and after a word or phrase. To bold and italicize the middle of a word for emphasis, add three asterisks without spaces around the letters.

| Markdown                                  | HTML                                                          | Rendered Output                        |
| ----------------------------------------- | ------------------------------------------------------------- | -------------------------------------- |
| `This text is ***really important***.`    | `This text is <em><strong>really important</strong></em>.`    | This text is _**really important**_.   |
| `This text is ___really important___.`    | `This text is <em><strong>really important</strong></em>.`    | This text is _**really important**_.   |
| `This text is __*really important*__.`    | `This text is <em><strong>really important</strong></em>.`    | This text is _**really important**_.   |
| `This text is **_really important_**.`    | `This text is <em><strong>really important</strong></em>.`    | This text is _**really important**_.   |
| `This is really***very***important text.` | `This is really<em><strong>very</strong></em>important text.` | This is really_**very**_important text |

> 📝 **Note:** The order of the em and strong tags might be reversed depending on the Markdown processor you're using.

#### Bold and Italic Best Practices

Markdown applications don’t agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to bold and italicize the middle of a word for emphasis.\
\| ✅ Do this | ❌ Don't do this |\
\| ----------------------------------------- | ----------------------------------------- |\
\| `This is really***very***important text.` | `This is really___very___important text.` |

## 6 Blockquotes

To create a blockquote, add a > in front of a paragraph.

```
> Dorothy followed her through many of the beautiful rooms in her castle. 
```

The rendered output looks like this:

> Dorothy followed her through many of the beautiful rooms in her castle.

### Blockquotes with Multiple Paragraphs

Blockquotes can contain multiple paragraphs. Add a `>` on the blank lines between the paragraphs.

```
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood. 
```

The rendered output looks like this:

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### Nested Blockquotes

Blockquotes can be nested. Add a `>>` in front of the paragraph you want to nest.

```
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood. 
```

The rendered output looks like this:

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### Blockquotes with Other Elements

Blockquotes can contain other Markdown formatted elements. Not all elements can be used — you’ll need to experiment to see which ones work.

```
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**. 
```

The rendered output looks like this:

> **The quarterly results look great!**
>
> * Revenue was off the chart.
> * Profits were higher than ever.
>
> _Everything_ is going according to **plan**.

> Blockquotes Best Practices

For compatibility, put blank lines before and after blockquotes.

| ✅ Do this                                                                                                | ❌ Don't do this                                                                                     |
| -------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| <p>Try to put a blank line before...<br><br>> This is a blockquote<br><br>...and after a blockquote.</p> | <p>Without blank lines, this might not look right.<br>> This is a blockquote<br>Don't do this!`</p> |

## 7 Lists

You can organize items into ordered and unordered lists.

### Ordered Lists

To create an ordered list, add line items with numbers followed by periods. The numbers don’t have to be in numerical order, but the list should start with the number one.

| Markdown                                                                                                                  | HTML                                                                                                                                                                                                                                                                                                                                                                                                                                  | Rendered Output                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| <p>1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item</p>                                                 | <p><code>&#x3C;ol></code><br>  <code>&#x3C;li>First item&#x3C;/li></code><br>  <code>&#x3C;li>Second item&#x3C;/li></code><br>  <code>&#x3C;li>Third item&#x3C;/li></code><br>  <code>&#x3C;li>Fourth item&#x3C;/li></code><br><code>&#x3C;/ol></code></p>                                                                                                                                                                            | <p>1.First item<br>2.Second item<br>3.Third item<br>4.Fourth item</p>                                               |
| <p>1. First item<br>1. Second item<br>1. Third item<br>1. Fourth item</p>                                                 | <p><code>&#x3C;ol></code><br>  <code>&#x3C;li>First item&#x3C;/li></code><br>  <code>&#x3C;li>Second item&#x3C;/li></code><br>  <code>&#x3C;li>Third item&#x3C;/li></code><br>  <code>&#x3C;li>Fourth item&#x3C;/li></code><br><code>&#x3C;/ol></code></p>                                                                                                                                                                            | <p>1.First item<br>2.Second item<br>3.Third item<br>4.Fourth item</p>                                               |
| <p>1. First item<br>8. Second item<br>3. Third item<br>5. Fourth item</p>                                                 | <p><code>&#x3C;ol></code><br>  <code>&#x3C;li>First item&#x3C;/li></code><br>  <code>&#x3C;li>Second item&#x3C;/li></code><br>  <code>&#x3C;li>Third item&#x3C;/li></code><br>  <code>&#x3C;li>Fourth item&#x3C;/li></code><br><code>&#x3C;/ol></code></p>                                                                                                                                                                            | <p>1.First item<br>2.Second item<br>3.Third item<br>4.Fourth item</p>                                               |
| <p>1. First item<br>2. Second item<br>3. Third item<br>    1. Indented item<br>    2. Indented item<br>4. Fourth item</p> | <p><code>&#x3C;ol></code><br>  <code>&#x3C;li>First item&#x3C;/li></code><br>  <code>&#x3C;li>Second item&#x3C;/li></code><br>  <code>&#x3C;li>Third item&#x3C;/li></code><br>    <code>&#x3C;ol></code><br>      <code>&#x3C;li>Indented item&#x3C;/li></code><br>      <code>&#x3C;li>Indented item&#x3C;/li></code><br>    <code>&#x3C;/ol></code><br>  <code>&#x3C;li>Fourth item&#x3C;/li></code><br><code>&#x3C;/ol></code></p> | <p>1.First item<br>2.Second item<br>3.Third item<br>    1.Indented item<br>    2.Indented item<br>4.Fourth item</p> |

#### Ordered List Best Practices

CommonMark and a few other lightweight markup languages let you use a parenthesis ()) as a delimiter (e.g., 1) First item), but not all Markdown applications support this, so it isn’t a great option from a compatibility perspective. For compatibility, use periods only.

| ✅ Do this                              | ❌ Don't do this                        |
| -------------------------------------- | -------------------------------------- |
| <p>1. First item<br>2. Second item</p> | <p>1) First item<br>2) Second item</p> |

### Unordered Lists

To create an unordered list, add dashes (-), asterisks (\*), or plus signs (+) in front of line items. Indent one or more items to create a nested list.

| Markdown                                                                                                                  | HTML                                                                                                                                                                                                                                                                                                                                                                                                                                  | Rendered Output                                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>- First item<br>- Second item<br>- Third item<br>- Fourth item</p>                                                     | <p><code>&#x3C;ul></code><br>  <code>&#x3C;li>First item&#x3C;/li></code><br>  <code>&#x3C;li>Second item&#x3C;/li></code><br>  <code>&#x3C;li>Third item&#x3C;/li></code><br>  <code>&#x3C;li>Fourth item&#x3C;/li></code><br><code>&#x3C;/ul></code></p>                                                                                                                                                                            | <ul><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ul>                                                             |
| <p><code>* First item</code><br><code>* Second item</code><br><code>* Third item</code><br><code>* Fourth item</code></p> | <p><code>&#x3C;ul></code><br>  <code>&#x3C;li>First item&#x3C;/li></code><br>  <code>&#x3C;li>Second item&#x3C;/li></code><br>  <code>&#x3C;li>Third item&#x3C;/li></code><br>  <code>&#x3C;li>Fourth item&#x3C;/li></code><br><code>&#x3C;/ul></code></p>                                                                                                                                                                            | <ul><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ul>                                                             |
| <p><code>+ First item</code><br><code>+ Second item</code><br><code>+ Third item</code><br><code>+ Fourth item</code></p> | <p><code>&#x3C;ul></code><br>  <code>&#x3C;li>First item&#x3C;/li></code><br>  <code>&#x3C;li>Second item&#x3C;/li></code><br>  <code>&#x3C;li>Third item&#x3C;/li></code><br>  <code>&#x3C;li>Fourth item&#x3C;/li></code><br><code>&#x3C;/ul></code></p>                                                                                                                                                                            | <ul><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ul>                                                             |
| <p>- First item<br>- Second item<br>- Third item<br>    - Indented item<br>    - Indented item<br>- Fourth item</p>       | <p><code>&#x3C;ul></code><br>  <code>&#x3C;li>First item&#x3C;/li></code><br>  <code>&#x3C;li>Second item&#x3C;/li></code><br>  <code>&#x3C;li>Third item&#x3C;/li></code><br>    <code>&#x3C;ul></code><br>      <code>&#x3C;li>Indented item&#x3C;/li></code><br>      <code>&#x3C;li>Indented item&#x3C;/li></code><br>    <code>&#x3C;/ul></code><br>  <code>&#x3C;li>Fourth item&#x3C;/li></code><br><code>&#x3C;/ul></code></p> | <ul><li>First item</li><li>Second item</li><li><p>Third item</p><ul><li>Indented item</li><li>Indented item</li></ul></li><li>Fourth item</li></ul> |

#### Starting Unordered List Items With Numbers

If you need to start an unordered list item with a number followed by a period, you can use a backslash (`\`) to escape the period.

| Markdown                                                        | HTML                                                                                                                                                                                 | Rendered Output                                                             |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| <p>- 1968. A great year!<br>- I think 1969 was second best.</p> | <p><code>&#x3C;ul></code><br>  <code>&#x3C;li>1968. A great year!&#x3C;/li></code><br>  <code>&#x3C;li>I think 1969 was second best.&#x3C;/li></code><br><code>&#x3C;/ul></code></p> | <ul><li>1968. A great year!</li><li>I think 1969 was second best.</li></ul> |

#### Unordered List Best Practices

Markdown applications don’t agree on how to handle different delimiters in the same list. For compatibility, don’t mix and match delimiters in the same list — pick one and stick with it.

| ✅ Do this                                                                                                                 | ❌ Don't do this                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| <p><code>- First item</code><br><code>- Second item</code><br><code>- Third item</code><br><code>- Fourth item</code></p> | <p><code>+ First item</code><br><code>* Second item</code><br><code>- Third item</code><br><code>+ Fourth item</code></p> |

### Adding Elements in Lists

To add another element in a list while preserving the continuity of the list, indent the element four spaces or one tab, as shown in the following examples.

> 💡 **Tip:** If things don't appear the way you expect, double check that you've indented the elements in the list four spaces or one tab.

#### Paragraphs

```
* This is the first list item.
* Here's the second list item.

    > I need to add another paragraph below the second list item.

* And here's the third list item. 
```

The rendered output looks like this:

* This is the first list item.
*   Here’s the second list item.

    > I need to add another paragraph below the second list item.
* And here’s the third list item.

#### Blockquotes

```
* This is the first list item.
* Here's the second list item.

    > A blockquote would look great below the second list item.

* And here's the third list item. 
```

The rendered output looks like this:

* This is the first list item.
*   Here’s the second list item.

    > A blockquote would look great below the second list item.

#### Code blocks

[Code Blocks](app://obsidian.md/index.html#Code%20Blocks) are normally indented four spaces or one tab. When they’re in a list, indent them eight spaces or two tabs.

```
1. Open the file.
2. Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3. Update the title to match the name of your website. 
```

The rendered output looks like this:

1. Open the file.
2.  Find the following code block on line 21:

    ```
     <html>
       <head>
         <title>Test</title>
       </head> 
    ```
3. Update the title to match the name of your website.

#### Images

```
1. Open the file containing the Linux mascot.
2. Marvel at its beauty.

    ![Tux, the Linux mascot](/assets/images/tux.png)

3. Close the file. 
```

The rendered output looks like this:

1. Open the file containing the Linux mascot.
2.  Marvel at its beauty.

    ![Tux, the Linux mascot](https://mdg.imgix.net/assets/images/tux.png)
3. Close the file.

#### Lists

You can nest an unordered list in an ordered list, or vice versa.

```
1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item 
```

The rendered output looks like this:

1. First item
2. Second item
3. Third item
   * Indented item
   * Indented item
4. Fourth item

## 8 Code

To denote a word or phrase as code, enclose it in backticks (`` ` ``).

| Markdown                                | HTML                                             | Rendered Output                     |
| --------------------------------------- | ------------------------------------------------ | ----------------------------------- |
| ``At the command prompt, type `nano`.`` | `At the command prompt, type <code>nano</code>.` | At the command prompt, type `nano`. |

### Escaping Backticks

If the word or phrase you want to denote as code includes one or more backticks, you can escape it by enclosing the word or phrase in double backticks (` `` `).

| Markdown                                      | HTML                                               | Rendered Output                       |
| --------------------------------------------- | -------------------------------------------------- | ------------------------------------- |
| ``` ``Use `code` in your Markdown file.`` ``` | ``<code>Use `code` in your Markdown file.</code>`` | ``Use `code` in your Markdown file.`` |

### Code Blocks

To create code blocks, indent every line of the block by at least four spaces or one tab.

```
 <html>
    <head>
    </head>
</html> 
```

The rendered output looks like this:

```html
<html>
  <head>
  </head>
</html> 
```

\> 📝 \*\*Note:\*\* To create code blocks without indenting lines, use \[\[MarkdownExtended#Fenced Code Blocks|fenced code blocks]].

## 9 Horizontal Rules

To create a horizontal rule, use three or more asterisks (`***`), dashes (`---`), or underscores (`___`) on a line by themselves.

```
***

---

_________________ 
```

The rendered output of all three looks identical:

***

> Horizontal Rule Best Practices

For compatibility, put blank lines before and after horizontal rules.

| ✅ Do this                                                                                               | ❌ Don't do this                                                                            |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| <p>Try to put a blank line before...<br><br><code>---</code><br><br>...and after a horizontal rule.</p> | <p>Without blank lines, this would be a heading.<br><code>---</code><br>Don't do this!</p> |

## 10 Links

To create a link, enclose the link text in brackets (e.g., `[Duck Duck Go]`) and then follow it immediately with the URL in parentheses (e.g., `(https://duckduckgo.com)`).

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com). 
```

The rendered output looks like this:

My favorite search engine is [Duck Duck Go](https://duckduckgo.com/).

> 📝 **Note:** To link to an element on the same page, see linking to [heading IDs](app://obsidian.md/MarkdownExtended#Heading%20IDs). To create a link that opens in a new tab or window, see the section on [link targets](app://obsidian.md/MarkdownAdvance#Link%20Targets).

### Adding Titles

You can optionally add a title for a link. This will appear as a tooltip when the user hovers over the link. To add a title, enclose it in quotation marks after the URL.

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy"). 
```

The rendered output looks like this:

My favorite search engine is [Duck Duck Go](https://duckduckgo.com/).

### URLs and Email Addresses

To quickly turn a URL or email address into a link, enclose it in angle brackets.

```
<https://www.markdownguide.org>
<fake@example.com> 
```

The rendered output looks like this:

[https://www.markdownguide.org](https://www.markdownguide.org/)\
[fake@example.com](mailto:fake@example.com)

### Formatting Links

To [emphasize](app://obsidian.md/index.html#Emphasis) links, add asterisks before and after the brackets and parentheses. To denote links as [code](app://obsidian.md/index.html#Code), add backticks in the brackets.

```
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code). 
```

The rendered output looks like this:

I love supporting the [**EFF**](https://eff.org/).\
This is the [_Markdown Guide_](https://www.markdownguide.org/).\
See the section on [code](app://obsidian.md/index.html#Code).

### Reference-style Links

Reference-style links are a special kind of link that make URLs easier to display and read in Markdown. Reference-style links are constructed in two parts: the part you keep inline with your text and the part you store somewhere else in the file to keep the text easy to read.

#### Formatting the First Part of the Link

The first part of a reference-style link is formatted with two sets of brackets. The first set of brackets surrounds the text that should appear linked. The second set of brackets displays a label used to point to the link you’re storing elsewhere in your document.

Although not required, you can include a space between the first and second set of brackets. The label in the second set of brackets is not case sensitive and can include letters, numbers, spaces, or punctuation.

This means the following example formats are roughly equivalent for the first part of the link:

* `[hobbit-hole][1]`
* `[hobbit-hole] [1]`

#### Formatting the Second Part of the Link

The second part of a reference-style link is formatted with the following attributes:

1. The label, in brackets, followed immediately by a colon and at least one space (e.g., `[label]:` ).
2. The URL for the link, which you can optionally enclose in angle brackets.
3. The optional title for the link, which you can enclose in double quotes, single quotes, or parentheses.

This means the following example formats are all roughly equivalent for the second part of the link:

* `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle`
* `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"`
* `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'`
* `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)`
* `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"`
* `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit lifestyles'`
* `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)`

You can place this second part of the link anywhere in your Markdown document. Some people place them immediately after the paragraph in which they appear while other people place them at the end of the document (like endnotes or footnotes).

#### An Example Putting the Parts Together

Say you add a URL as a [standard URL link](app://obsidian.md/index.html#Links) to a paragraph and it looks like this in Markdown:

```
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort. 
```

Though it may point to interesting additional information, the URL as displayed really doesn’t add much to the existing raw text other than making it harder to read. To fix that, you could format the URL like this instead:

```
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole][1], and that means comfort.

[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles" 
```

In both instances above, the rendered output would be identical:

> In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle), and that means comfort.

and the HTML for the link would be:

```html
<a href="https://en.wikipedia.org/wiki/Hobbit#Lifestyle" title="Hobbit lifestyles">hobbit-hole</a> 
```

> Link Best Practices

Markdown applications don’t agree on how to handle spaces in the middle of a URL. For compatibility, try to URL encode any spaces with `%20`. Alternatively, if your Markdown application [supports HTML](app://obsidian.md/index.html#HTML), you could use the `a` HTML tag.

| ✅ Do this                                                                                                                                                    | ❌ Don't do this                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------- |
| <p><code>[link](https://www.example.com/my%20great%20page)</code><br><br><code>&#x3C;a href="https://www.example.com/my great page">link&#x3C;/a></code></p> | `[link](https://www.example.com/my great page)` |

## 11 Images

To add an image, add an exclamation mark (`!`), followed by alt text in brackets, and the path or URL to the image asset in parentheses. You can optionally add a title in quotation marks after the path or URL.

```
![The San Juan Mountains are beautiful!](/assets/images/san-juan-mountains.jpg "San Juan Mountains") 
```

The rendered output looks like this:

![The San Juan Mountains are beautiful!](https://mdg.imgix.net/assets/images/san-juan-mountains.jpg)

> 📝 **Note:** To resize an image, see the section on [image size](app://obsidian.md/MarkdownAdvance#Image%20Size). To add a caption, see the section on [image captions](app://obsidian.md/\[MarkdownAdvance#Image%20Captions).

### Linking Images

To add a link to an image, enclose the Markdown for the image in brackets, and then add the link in parentheses.

```
[![An old rock in the desert](/assets/images/shiprock.jpg "Shiprock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv) 
```

The rendered output looks like this:

[![An old rock in the desert](https://mdg.imgix.net/assets/images/shiprock.jpg)](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)

## 12 Escaping Characters

To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash (`\`) in front of the character.

```
\* Without the backslash, this would be a bullet in an unordered list. 
```

The rendered output looks like this:

\* Without the backslash, this would be a bullet in an unordered list.

> Characters You Can Escape

You can use a backslash to escape the following characters.

<table><thead><tr><th width="162">Character</th><th>Name</th></tr></thead><tbody><tr><td>\</td><td>backslash</td></tr><tr><td>`</td><td>backtick (see also [[#Escaping Backticks</td></tr><tr><td>*</td><td>asterisk</td></tr><tr><td>_</td><td>underscore</td></tr><tr><td>{ }</td><td>curly braces</td></tr><tr><td>[ ]</td><td>brackets</td></tr><tr><td>&#x3C; ></td><td>angle brackets</td></tr><tr><td>( )</td><td>parentheses</td></tr><tr><td>#</td><td>pound sign</td></tr><tr><td>+</td><td>plus sign</td></tr><tr><td>-</td><td>minus sign (hyphen)</td></tr><tr><td>.</td><td>dot</td></tr><tr><td>!</td><td>exclamation mark</td></tr><tr><td>|</td><td>pipe (see also [[MarkdownExtended#Escaping Pipe Characters in Tables</td></tr></tbody></table>

## 13 HTML

Many Markdown applications allow you to use HTML tags in Markdown-formatted text. This is helpful if you prefer certain HTML tags to Markdown syntax. For example, some people find it easier to use HTML tags for images. Using HTML is also helpful when you need to change the attributes of an element, like specifying the [color of text](app://obsidian.md/MarkdownAdvance#Color) or changing the width of an image.

To use HTML, place the tags in the text of your Markdown-formatted file.

```
This **word** is bold. This <em>word</em> is italic. 
```

The rendered output looks like this:

This **word** is bold. This _word_ is italic.

> HTML Best Practices

For security reasons, not all Markdown applications support HTML in Markdown documents. When in doubt, check your Markdown application’s documentation. Some applications support only a subset of HTML tags.

Use blank lines to separate block-level HTML elements like `<div>`, `<table>`, `<pre>`, and `<p>` from the surrounding content. Try not to indent the tags with tabs or spaces — that can interfere with the formatting.

You can’t use Markdown syntax inside block-level HTML tags. For example, `<p>italic and **bold**</p>` won’t work.

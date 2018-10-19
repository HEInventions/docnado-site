 title:      Markdown The docnado Way!
 desc:       An introduction to Markdown and docnado's additional features.
 date:       2018/10/12
 version:    1.0.0
 template:   document
 nav:        Getting Started>Creating a Document 
 percent:    100
 authors:    enq@heinventions.com

When creating documentation it's important to use a markup language that semantically structures your text that's both easy for less technically inclined users to create and modify, but fully featured enough to deliver your documentation the way you need. To achieve this docnado uses [`markdown`](https://en.wikipedia.org/wiki/Markdown), with it's own added features to style your documentation and present images, videos, and other multimedia the way you want.

# Markdown
Markdown on it's own is a powerful tool for presenting text information, with it you can create:

* Headings
* Tables
* Emphasis
* Lists
* Hyperlinks
* Code blocks and syntax highlighting
* Blockquotes
* Horizontal Rules
* Embedded HTML

This page starts with a quick introduction to markdown and it's features and how you can use them in a docnado document. For a more complete information please see [The Original Specification](https://daringfireball.net/projects/markdown/).

## Headings
In order to mark the beginning of a section, subsection, or paragraph you can use the *header* tag. This is indicated by a hash symbol (`#`) followed by a space, the text you want to use, and then finally a newline. To create sub-headings you can use multiple hash symbols to indicate a lower precedence. Up to six hashes may be used.

```markdown
# Header 
## Nested Header
### Doubly Nested Header
#### Nested Again
##### And Again
###### Phew! This is as deep as it goes I'm afraid.
```
# Header 
## Nested Header
### Doubly Nested Header
#### Nested Again
##### And Again
###### Phew! This is as deep as it goes I'm afraid.
---
## Emphasis
**Sometimes** you need to be _emphatic_ in your documentation, luckily markdown has tools to do this for you.

All you have to do is surround the word or phrase you wish to emphasise with single asterisks (`*`), double asterisks (`**`), or underscores (`_`). You can also ~~strike through~~ text by surrounding your phrase with a double tilde (`~~`).

```markdown
Emphasis, sometimes called italics: *this is emphasised* and _so is this_

Strong Emphasis, also called bold: **this is strongly emphasised** and __so is this__

__The emphasis *symbols* can also be *nested*__
```

Emphasis, sometimes called italics: *This is emphasised* and _so is this_

Strong Emphasis, also called bold: **This is strongly emphasised** and __so is this__

__The emphasis *symbols* can also be *nested*__
---
## Lists
Markdown can be used to create lists of items, both ordered and unordered. These lists can also have ordered and unordered sublets.

An ordered list item can be simply created by tying a number, followed by a period (`.`), and ended with a new line. Unordered lists are created in much the same way but instead of a number you must use an asterisk (`*`), a dash (`-`), or a plus (`+`).

You can also format paragraphs within lists by beginning a new line below a list item with a tab.

```markdown
1. The first item in an ordered list.
	* Unordered sub-list item one.
	* Unordered sub-list item two.

2. The second item in an ordered list.

	A new line in the paragraph that runs on from the second item in the ordered list.  
	A second new line in the paragraph. The preceding line must end in a double space to avoid starting a new paragraph.

3. The third item in an ordered list.

+ An unordered list created with a plus.
	1. Ordered sub-list item one.
	2. Ordered sub-list item two.

* Unordered list item two created with an asterisk.

- Unordered list item three created with a dash.
```

1. The first item in an ordered list.
	* Unordered sub-list item one.
	* Unordered sub-list item two.

2. The second item in an ordered list.

	A new line in the paragraph that runs on from the second item in the ordered list.  
	A second new line in the paragraph. The preceding line must end in a double space to avoid starting a new paragraph.

3. The third item in an ordered list.

+ An unordered list created with a plus.
	1. Ordered sub-list item one.
	2. Ordered sub-list item two.

* Unordered list item two created with an asterisk.

- Unordered list item three created with a dash.

Usefully, docnado also supports other list styles:

# Progress Lists
A progress list is a list of check boxes:

* [ ] This is one.
* [X] This is two. It happens to be a long list item designed to test how the styling copes with the multiples lines generated.
* [ ] This is three.
```markdown
* [ ] This is one.
* [X] This is two. It happens to be a long list item designed to test how the styling copes with the multiples lines generated.
* [ ] This is three.
```

# Definition Lists
Glossary-style definition lists are achieved as follows:

Apple
:   Pomaceous fruit of plants of the genus Malus in
    the family Rosaceae.

Orange
:   The fruit of an evergreen tree of the genus Citrus.

```markdown
Apple
:   Pomaceous fruit of plants of the genus Malus in
    the family Rosaceae.

Orange
:   The fruit of an evergreen tree of the genus Citrus.
```
---
## Tables
A documentation project can often involve lots of tabular data, components with their pricing and order number, staff and their contact details etc. Luckily docnado supports the simple creation of tables in your document.

Simply separate columns wish a pipe character (`|`) and rows with newlines. The head of the table is separated by lines of at least three dashes (`---`) in each cell of the 2nd line of a table.

More dashes can be used for readability.
{: .info}

```markdown
| Table Heading One               | Table Heading Two | Table Heading Three      |
|---------------------------------|-------------------|--------------------------|
|Table Item                       | Table item two    | Table item three         |
| This                            | is                | a row                    |
| Inside a table you can still use| _emphasis_        | and __strong emphasis__  |
```

| Table Heading One               | Table Heading Two | Table Heading Three      |
|---------------------------------|-------------------|--------------------------|
|Table Item                       | Table item two    | Table item three         |
| This                            | is                | a row                    |
| Inside a table you can still use| _emphasis_        | and __strong emphasis__  |

Most inline markdown syntax can still be used within a table including hyperlinks, emphasis and, inline code blocks.

Tables are not a part of the standard markdown specification, but Docserve (and other markdown rendering tools) support this style as the _de facto_ standard.
{: .info}

At the moment, tables defined in Markdown are **not** stylable using style classes `{: .my-table}`.
{: .warning}


### External CSV Tables

You can include tables from CSV files. These will be loaded and inserted into the Markdown.

```markdown
![](assets/example.csv)
```

![](assets/example.csv)

Tables included from a `.csv` file can have styles applied. For example, `.full-width` makes the table stretch to fill the entire area.

```markdown
![](assets/example.csv){: .full-width}
```

![](assets/example.csv){: .full-width}
---
## Hyperlinks and Images
Linking to other pages of your documentation or to pages on the wider web can be done with the hyperlink syntax.

Creating a link to a web-page and be achieved by surrounding the word or phrase you want to make into a link with square brackets (`[` and `]`) and following it with the location of the website you want to link to, surrounded by parentheses (`(` and `)`). Alt-text can be added by using speech marks (`"`) after the web address, but this is optional.

For example:
```markdown
This is a sentence with a link to the [Google Homepage](http://www.google.co.uk "Google Search Homepage") in it.
```

This is a sentence with a link to the [Google Homepage](http://www.google.co.uk "Google Search Homepage") in it.

Another useful feature is reference style linking. You can create a list of web links anywhere within your document (we recommend at the end) and re-use them throughout your document.

```markdown
[Google]: http://www.google.co.uk
[Twitter]: http://www.twitter.com
[Wikipedia]: http://en.wikipedia.org

These links go to [Google], [Twitter's Homepage][Twitter], and [Wikipedia]
``` 

[Google]: http://www.google.co.uk
[Twitter]: http://www.twitter.com
[Wikipedia]: http://en.wikipedia.org

These links go to [Google], [Twitter's Homepage][Twitter], and [Wikipedia]

Embedding images in your docnado documents follows a similar syntax, but should be preceded by an exclamation mark (`!`). In this case the text within square brackets functions as image alt-text.

```markdown
Inline 
![docnado](assets/logo.png "docnado, blow your documentation away!")

![alt text][logo]

[logo]: /assets/logo.png "Logo Title Text 2"
```

![docnado](assets/logo.png "docnado, blow your documentation away!")

[logo]: assets/logo.png "docnado, blow your documentation away!"

![docnado Image 2 ][logo]

docnado also supports the styling of images, this can be done by adding an inline style tag after your image.

```markdown
<!-- Example --> 
<!-- A row of 3 images --> 
![](assets/logo.png){: .small}
![](assets/logo.png){: .small}
![](assets/logo.png){: .small}

<!-- Style classes can be combined. --> 
![](assets/logo.png){: .small .noborder}

<!-- We can put them in the middle. --> 
![](assets/logo.png){: .small .center}

<!-- Make them middle sized. --> 
![](assets/logo.png){: .medium}

<!-- The default is actual width up to a max height of the document flow, and no higher than a single A4 page. --> 
![](assets/logo.png)

<!-- The style class .large is the same as the default. --> 
![](assets/logo.png){: .large}
```

Unlike paragraphs, images are *inline* elements, so the style `{: style-class}` needs to be on the same line as the element.
{: .info}

This is an inline ![](assets/logo.png){: .icon} icon.

![](assets/logo.png){: .small}
![](assets/logo.png){: .small}
![](assets/logo.png){: .small}

![](assets/logo.png){: .small .noborder}

![](assets/logo.png){: .small .center}

![](assets/logo.png){: .medium}

![](assets/logo.png)

![](assets/logo.png){: .large}
---
# Multimedia
docnado also supports the ability to embed a plethora of media types, including videos:

```markdown
![](assets/big_buck_bunny.ogv){: .small}

![](assets/big_buck_bunny.ogv){: .medium}

![](assets/big_buck_bunny.ogv)
```

Supported formats include: `.ogv`, `.ogg`, `webm`, `mp4`, and in some browsers `avi`.
{: .info}

![](assets/big_buck_bunny.ogv){: .small}

![](assets/big_buck_bunny.ogv){: .medium}

![](assets/big_buck_bunny.ogv)

Embedded Youtube videos: 

```markdown
![](https://www.youtube.com/embed/Jg48NhtIDV8){: .small}

![](https://www.youtube.com/embed/Jg48NhtIDV8){: .medium}

![](https://www.youtube.com/embed/Jg48NhtIDV8)
```

![](https://www.youtube.com/embed/Jg48NhtIDV8){: .small}

![](https://www.youtube.com/embed/Jg48NhtIDV8){: .medium}

![](https://www.youtube.com/embed/Jg48NhtIDV8)

PDF documents:

```markdown
![](assets/example.pdf)

![](assets/example.pdf){: .landscape}
```

![](assets/example.pdf)

![](assets/example.pdf){: .landscape}

You can add a `{: .landscape}` property to these in order to change the aspect ratio. Only the `A4` paper aspect is currently supported.
{:.tip}


---
## Code blocks and syntax highlighting
What if you're documenting a software product, or writing up a coding tutorial (like this one for example!)? docnado has you covered, you can create blocks of example code with syntax highlighting.

Simply use three backticks (` ``` `) followed by the language you wish to use.

```markdown
 ```C
#include <stdio.h>

main() {
        printf("Hello, World\n");
}
 ```
```
```C
#include <stdio.h>

main() {
        printf("Hello, World\n");
}
```


You code blocks can also be used in an inline style, by putting a single backtick before and after your code sample, but remember docnado does not support highlighting in this mode. 

```markdown
This is an example of how to use inline code blocks `C = map(lambda x: (float(5)/9)*(x-32), Fahrenheit)`. Cool!
```

This is an example of how to use inline code blocks `C = map(lambda x: (float(5)/9)*(x-32), Fahrenheit)`. Cool!

docnado uses highlight.js for this highlighting feature and therefore supports every language highlight.js does!
{: .info}

---
## Blockquotes
Blockquotes are a text block that is generally used for showing quotations. They are useful for any discussion on a project, email or other document quotations, or for just being motivational!

You declare them by simply using a greater-than symbol followed by a space (`> `)  at the start of each line and end them with a new line.

```markdown
>"Do not meddle in the affairs of wizards, for they are subtle and quick to anger!" - J.R.R Tolkien
```
>"Do not meddle in the affairs of wizards, for they are subtle and quick to anger!" - J.R.R Tolkien

---
## Horizontal Rules
Horizontal Rules are great for creating a visual horizontal separation in your documentation, use them to separate logical sections of a document. They are created by creating three consecutive hyphens (`---`), asterisks (`***`), or underscores (`___`) at the start of a new line.

```markdown
This text is followed by a horizontal rule.
___
So is this one
---
And this one is too!
***
```
This text is followed by a horizontal rule.
___

So is this one
---
And this one is too!
***

## Embedded HTML
{ .warning }

Embedding HTML within Docserve documents is also supported.

```markdown
#### A Sample Document
<marquee>This is a Docserve document with embedded HTML!</marquee>
```
#### A Sample Document
<marquee>This is a Docserve document with embedded HTML!</marquee>

# Callouts
Often when writing documentation you want to draw your audience's attention in some way, perhaps to a safety warning or operational tip. docnado does this with our callout tags!

Simply follow a line with a tag describing which style of callout you want to use. The available tags are:

* {: .info}
* {: .warning}
* {: .danger}
*  {: .tip}

*
*

```markdown
Informative style callouts go here.
{: .info}

Warning style callouts can be added too. Keep them punchy.
{: .warning}

Dangerous warnings go here.
{: .danger}

Take a look at the Markdown file to see how these are implemented.
{: .tip}
```

Informative style callouts go here.
{: .info}

Warning style callouts can be added too. Keep them punchy.
{: .warning}

Dangerous warnings go here.
{: .danger}

Take a look at the Markdown file to see how these are implemented.
{: .tip}

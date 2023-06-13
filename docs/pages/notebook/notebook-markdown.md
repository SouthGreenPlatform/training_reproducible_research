## A markup language

A *markup language* is a system for annotating text documents in order to
*e.g.* define formatting. HTML, if you are familiar with that, is an example of
a markup language. HTML uses tags, such as:

```html title="Example in HTML"
<h1>Heading</h1>
<h2>Sub-heading</h2>
<a href="www.webpage.com">Link</a>
<ul>
  <li>List-item1</li>
  <li>List-item2</li>
  <li>List-item3</li>
</ul>
```

and this is the result :

<h1>Heading</h1>
<h2>Sub-heading</h2>
<a href="http://example.com">Link</a>
<ul>
  <li>List-item1</li>
  <li>List-item2</li>
  <li>List-item3</li>
</ul>

## Markdown

*Markdown* is a lightweight markup language which uses plain-text syntax in
order to be as unobtrusive as possible, so that a human can easily read it.
The code below gives the same result as the HTML code shown above : 

```markdown title="Example in markdown"
# Heading

## Sub-heading

### Another deeper heading

A [link](http://example.com).

Text attributes _italic_, *italic*, **bold**, `monospace`.

Bullet list:

  * apples
  * oranges
  * pears
```

A markdown document can be converted to other formats, such as HTML or PDF, for
viewing in a browser or a PDF reader. For example, the page you are reading right now is
written in markdown. Markdown is somewhat ill-defined, and as a consequence of
that there exist many implementations and extensions, although they share most
of the syntax. *R Markdown* is one such implementation/extension.

A large number of sites give you the full syntax of Markdonw. Below is a cheat sheet 
proposed by GitHUb : 

<iframe id="iframepdf" src="../../cheat_sheet/notebook/markdown-cheatsheet.pdf" frameborder="0" width="100%" height="600" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe> 

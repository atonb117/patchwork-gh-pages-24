---
layout: page
title: Markdown
permalink: /markdown/
---

<!--
This is an HTML comment. It won't show up on your page, but it does show up in the source code.

This file might be helpful as you learn more about markdown. However, you probably don't want it appearing on your final web page. Feel free to remove it from your site at any time.

A permanent copy is found below, so if you do remove it you can still have access to the contents. We've also included it in an "issue" in your GitHub repo: navigate to the "Issues" tab to find it.
-->

Markdown is a simple, human-readable markup language. In other words, it's a way to format plaintext in a way that is easy to read and write as plaintext, and which a program like Jekyll can then take and format easily.

A lot of sites use markdown. You may have seen it in blog comments, reddit posts, or GitHub issues. It's popular because it's so easy to use. GitHub Pages and Jekyll use markdown to define the content of websites so you don't have to write HTML and CSS unless you're redesigning the site.

In this lesson, we're going to go over the basics of markdown, as well as some GitHub-specific features. By the end, you'll be able to use markdown not only to produce beautiful Jekyll sites, but also around the web.

A permanent copy of this page can be found at <a href="http://wheelhouseio.github.io/project-gh-pages/markdown/" target="_blank">wheelhouseio.github.io/project-gh-pages/markdown</a>.

---

## Basic Text Formatting

### Paragraphs
Let's start simple. Most text in markdown is just written as plaintext. To create a new paragraph, simply hit the "return/enter" button twice to create a blank line between your two paragraphs.

{% highlight markdown %}
This is a paragraph.

This is another paragraph.
{% endhighlight %}

> This is a paragraph.
> 
> This is another paragraph.

### Bold
Say you're writing a message, and you want one part to be highlighted to the recipient is more likely to pay attention to it. You bold the message. In markdown, you bold text by wrapping it in two asterixes.

{% highlight markdown %}
This text is plain, **this text is bold**.
{% endhighlight %}

> This text is plain, **this text is bold**.

The wrapped text will end up bold in the final project.

### Italics
If you want to italitize some text, you can wrap it with a single underscore character on each side.

{% highlight markdown %}
We're reading _My Brilliant Friend_ in our book club this month.
{% endhighlight %}

> We're reading _My Brilliant Friend_ in our book club this month.

Using a single asterisk will also work if you don't like the looks of the underscore character.

### Formatting across paragraphs.
Bolding, italicizing, and striking out are all line-level formats. That is to say, they won't work across paragraphs. For instance, if you want to bold two whole paragraphs, you'll have to separately mark each one as bolded.

{% highlight markdown %}
**Bold paragraph the first.**

**Bold paragraph the second.**
{% endhighlight %}

> **Bold paragraph the first.**
> 
> **Bold paragraph the second.**

### Headers
Headers are created using hash marks before the text designed to be a header. The entire paragraph will become a header. A header can have one to six hash marks before it. The more hashes, the smaller the header will be.

{% highlight markdown %}
# Title

## Introduction

This is the introduction text.

## Chapter 1

This is the first chapter's text.
{% endhighlight %}

> # Title
> 
> ## Introduction
> 
> This is the introduction text.
> 
> ## Chapter 1
> 
> This is the first chapter's text.

All of the headers look like this: 

{% highlight markdown %}
# Header 1

## Header 2

### Header 3

#### Header 4

##### Header 5

###### Header 6

####### Not a header
{% endhighlight %}

---

## Document formatting

Sometimes you need to do more than just make paragraphs and mark up the text inside of them. Markdown includes methods for creating lists, quoted text, and more.

### Lists

There are two types of lists in markdown, **ordered lists** and **unordered lists**.

#### Unordered Lists

To create an unordered list, you put an asterix at the beginning of each new item in the list, and separate the items by a single new line.

{% highlight markdown %}
* Item 1
* Item 2
* Item 3
{% endhighlight %}

> * Item 1
> * Item 2
> * Item 3

Unordered lists have a bullet placed before each item.

Dashes and pluses can also be used to create list items, so this is a valid list:

{% highlight markdown %}
- Item 1
+ Item 2
* Item 3
{% endhighlight %}

Some people prefer to use dashes or plus symbols because they are not used anywhere else in markdown formatting, but others prefer to use the asterisk because it looks more like a bullet. The choice is up to you!

#### Ordered Lists

To create an ordered lists, instead of putting an asterisk, dash, or plus before the list item, you put a number and a period.

{% highlight markdown %}
1. Item 1
2. Item 2
3. Item 3
{% endhighlight %}

> 1. Item 1
> 2. Item 2
> 3. Item 3

No matter what order you place the numbers in your plaintext file, markdown will generate the correct numbers in the displayed version.

{% highlight markdown %}
10. Item 1
2. Item 2
9. Item 3
{% endhighlight %}

This markup will still generate a list that looks like this:

> 10. Item 1
> 2. Item 2
> 9. Item 3

#### List formatting

Whether ordered or unordered, all lists follow some simple rules.

You can embed sub-lists inside others by indenting the sub-lists.

{% highlight markdown %}
* Item 1
* Item 2
  * Sub-item 1
  * Sub-item 2
* Item 3
{% endhighlight %}

If you embed an ordered list inside another list, the numerical ordering will be unique for each sub-list.

{% highlight markdown %}
1. Item 1
2. Item 2
  1. Sub-item 1
  2. Sub-item 2
3. Item 3
  1. Sub-item 1
  2. Sub-item 2
{% endhighlight %}

Placing one or two newlines between list items will format the lists differently. Two newlines will space the items further part.

{% highlight markdown %}
1. Item 1
2. Item 2
{% endhighlight %}

> 1. Item 1
> 2. Item 2

{% highlight markdown %}
1. Item 1

2. Item 2
{% endhighlight %}

> 1. Item 1
> 
> 2. Item 2

You can include multiple paragraphs inside of a list by indenting the paragraphs by two spaces.

{% highlight markdown %}
1. Item 1, paragraph 1
  
  Item 1, paragraph 2
2. Item 2
{% endhighlight %}

> 1. Item 1, paragraph 1
>   
>   Item 1, paragraph 2
> 2. Item 2


### Blockquotes

Sometimes you want to quote a large chunk of text and put it off from the rest of the text. Blockquotes are a way to do this. To create a blockquote, add an greater-than sign at the beginning of the line of the paragraph you want to quote.

Blockquotes can be nested by adding multiple greater-than signs.

{% highlight markdown %}
Regular text.

> A quoted paragraph.
> 
> Another quoted paragraph.
> 
> > Whoa nested blockquotes.
> 
> Final paragraph.
{% endhighlight %}

> Regular text.
> 
> > A quoted paragraph.
> > 
> > Another quoted paragraph.
> > 
> > > Whoa nested blockquotes.
> > 
> > Final paragraph.

Blockquotes can be used in a variety of ways. For instance, we're using blockquotes to show how code will look once formatted.

### Code

There are two ways to demarkate code in your text.

Code will display in a monospaced font, and will escape any markdown formatting (so that you see the actual characters, not formatted text).

#### In-line Code

You can wrap a line of code in back-tic marks to make that line show up in a monospaced font.

{% highlight markdown %}
To **bold text**, `add **two asterisks**`.
{% endhighlight %}

> To **bold text**, `add **two asterisks**`.

#### Code Blocks

If you add 4 spaces at the beginning of a line, markdown will treat that whole line as code. Any spaces that you indent beyond the 4 will show up to the user, so that you can show embedded code blocks.

{% highlight markdown %}
    * List item 1
    * List item 2
      * List sub-item 1
{% endhighlight %}

>     * List item 1
>     * List item 2
>       * List sub-item 1


## Links, Images, and HTML

### Links

Links are the lifeblood of the internet. Linking to other pages on your own site, and other sites on the internet, is a vital function. You can easily create links in markdown.

The link syntax looks like this:

{% highlight markdown %}
[Go to GitHub](http://github.com).
{% endhighlight %}

Which produces the following link:

> [Go to GitHub](http://github.com).

Let's break that down. Inside the brackets, you find the text you want to display to the user. Directly after the brackets (no spaces!), you put a URL inside parentheses. This URL must start with `http://` or `https://`, or the link won't form.


### Images

Images work similarly to links.

{% highlight markdown %}
![A red panda.](https://upload.wikimedia.org/wikipedia/commons/2/25/Lesser_panda_standing.jpg)
{% endhighlight %}

> ![A red panda.](https://upload.wikimedia.org/wikipedia/commons/2/25/Lesser_panda_standing.jpg)

Importantly, the image link begins with an exclamation point. Without this, you'll simply link to an image.

After that comes the alternate text. Unlike with a link, this text will not be visible to most users. However, if the image does not load, or if the user uses a text-to-speech screen reader, then the text will become available to the user. Finally, you include a URL of the image itself just like you would of a link.

Images will show up as their original size, so it's recommended that you use small images. If you're good at web design, then you can resize them using the CSS files.


### HTML

Markdown works by being turned into HTML for your browser to read. As such, you can include HTML in your markdown documents, and it will work just fine. For instance, if you wanted to make sure that a link opened in a new window or tab, you could include the following markdown:

{% highlight markdown %}
Check out our [store](http://store.com)!

It's a lot better than our <a href="http://competitorsstore.com" target="_blank">competitor's store</a>.
{% endhighlight %}

The first link would load normally, and the second (because of the `target="_blank"` attribute) would load in a new window or tab.

We're not going to go into the details of HTML in this course, but if you'd like to learn more we're recommend check out one of the free tutorials online.
---
title: Example Support Article & Style Guide
description: >
  A model for future articles including xamples and conventions for formatting a variety of support article topics. 
keywords:
  - List
  - of
  - keywords
  - about
  - this
  - page
  - System76

facebookImage: /_social/article
twitterImage: /_social/article

hidden: false
---

## Start with a 2nd-level header. The "title" will be filled in from the yaml details above.

Summarize the purpose of the article in a sentence or two.

### Table of Contents supports up to header level 3.

Add line-breaks before and after headers. 

#### This will not show up in Table of Contents.

>**NOTE:** notes, alerts, cautions, etc. should be formatted like this.

### Collapsable Sections



## Naming Conventions

Pop!\_OS should be written out fully. Include a backslash "\" to negate italicization by the underscore "_".

Capitalize Ubuntu, Windows, and any other proper names of software projects or Linux distributions. If a project or company uses different capitalization, defer to that spelling and capitalization.

>**NOTE:** For example, Apple's operating system should be written as "macOS" not "Mac OS" or "OS X" because that is how they are branded and trade-marked. Likewise NVIDIA should be capitalized because they are branded that way.

Also capitalize names of applications and acronyms. WINE is a recursive acronym that means Wine is Not an Emulator. It should be written as "WINE". Firefox should be either "Firefox" or "Mozilla Firefox." With Chrome/Chromium based browsers be specific: "Google Chrome," is different from Chromium, Brave, Vivaldi or Microsoft Edge. All are based on Chrome.

When talking about wireless connectivity, the brand name "Wi-Fi" should be used.

System76 products should contain the product name, generation and abbreviated model name: Oryx Pro 7 (oryp7). Whenver possible, you should also link to available documentation for that model see [hyperlinks below](#hyperlinks).

## Text Formatting

### Lists

1. Where possible.

2. Number steps.

3. In a tutorial.

4. When in doubt, break it down.

If you are explaining a process, be careful how you present the steps and in what order.

- Bullet point.

- When the order doesn't matter.

- Lists are okay too.

- Be used.

- But should only.

### Hyperlinks

Hyperlinks can be added to documents by surrounding text with square brackets. The text inside the brackets will be highlighted. Place the desired URL in parentheses as shown below.

[surround links with brackets](https://example.hyperlink.to.article.com/page)

Support articles can also be linked to directly: E.g. [this article is found here](articles/example-article-style-guide). If the article exists on the support site, clicking on the hyperlink will navigate to that page.

To link to a specific sub-section of an article add the content tag: [like this](articles/example-article-style-guide#hyperlinks). Content tags are created through headers in the articles. To link directly to this section of this document you'd use th content tag `#hyperlinks`.

>**CAUTION:** Improper grammar can cause confusion and change the meaning of a sentence. When in doubt, include punctuation in the correct place. Add formatting for hyperlinks after the fact to make sure the sentence makes sense without the added formatting.

When referencing specific System76 products link to the technical documentation for that model (if applicable). For example, if discussing the Lemur 10 (lemp10), link to it like this: [Lemur 10 (lemp10)](https://tech-docs.system76.com/models/lemp10/README.html).

### Keyboard Shortcuts

### Code Formatting

When including instructions for Terminal commands, be sure to make it clear where the command starts, and where it ends. There are a few ways to do this.

Code blocks. Code blocks should include the `bash` flag in the formatting. 

    ```bash
    sudo apt update
    ```

Produces this output.

```bash
sudo apt update
```

Feel free to add comments to your commands if they will make things clearer. 

```bash
# refresh repositories
sudo apt update
# apply available upgrades to packages
sudo apt upgrade
```

If referencing a command used elsewhere in the document, or if the command is very short, in-line code formatting can be used. For example, the `apt` command we ran earlier.
 
Always leave an extra line at the end of your document.

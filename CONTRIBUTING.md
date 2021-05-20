# Contributing to this website

Welcome and thank you for considering contributing to the Nomads SAGGA website!

Reading and following these guidelines will help us make contributing to this website as easy as possible.

## Quicklinks

* [Getting Started](#getting-started)
    * [Issues](#issues)
    * [Pull Requests](#pull-requests)
* [Specific Contributions](#specific-contributions)
    * [Pages](#pages)
    * [Gallery Pages](#gallery-pages)

## Getting Started

Contributions are made to this repo via Issues and Pull Requests (PRs). Please search for existing Issues and PRs before creating your own.

The website is built using [Jekyll](https://jekyllrb.com/) and only requires basic knowledge of [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) to start contributing.

### Issues

Issues should be used to report problems with an existing page, request a new RPG page be included, or to discuss potential changes before a PR is created.

If you find an Issue that addresses the issue you want to raise, please add your own thoughts to the existing issue rather than creating a new one. Adding a [reaction](https://github.blog/2016-03-10-add-reactions-to-pull-requests-issues-and-comments/) can also help by indicating to our maintainers that a particular issue is affecting more than just the reporter.

### Pull Requests

PRs to our website are welcome and are the quickest way to get things added to the site. In general, PRs should do one of the following:

- Add a page to the site.
- Fix typos/grammar in existing pages.
- Handle style/layout issues.

They must be relevant to the Nomads (i.e. a page or gallery that relates to things we do).

For changes that significantly modify the website style, it's best to open an Issue to discuss your proposal first. This is not required but can save time creating and reviewing changes.

In general, we follow the ["fork-and-pull" Git workflow](https://github.com/susam/gitpr)

1. Fork the repository to your own Github account
2. Clone the project to your machine
3. Create a branch locally with a succinct but descriptive name
4. Commit changes to the branch
5. Following any formatting and testing guidelines specific to this repo
6. Push changes to your fork
7. Open a PR in our repository and follow the PR template so that we can efficiently review the changes.

## Specific Contributions

Some guidelines for specific types of contribution.

### Pages

Pages should be added by creting a new Markdown file in `_posts`. They will need at least the following header info:

```
---
layout: single
title: "Title"
permalink: /permalink-path/
---
``` 

Content below the header is then just a Markdown document. You can include HTML if needed but the [Miminimal Mistakes theme](https://mademistakes.com/work/minimal-mistakes-jekyll-theme/) we are using offers a lot of versatility.

### Gallery Pages

Gallery Pages must be created in the `_gallery` collection. They need the following info in their header:

```
---
layout: single
title:  "Gallery Title"
permalink: /gallery/gallery-title
header:
  teaser: /assets/img/year/image.ext
gallery:
  - url: /assets/img/year/anotherimage.ext
    image_path: /assets/img/year/anotherimage.ext
    alt: "A description of the image as alt text"
    title: "A caption for the picture"
---
```

Pick your favourite image for the teaser. All images should go into `/assets/img/year/` with a filename like so `yearmonth-description.ext`.

As the gallery displays in a collection at `/gallery` it is nice to have an excerpt that describes the gallery. Write a sentence that describes the gallery then add the following on a new line:

```
<!--more-->
```

You can then add any furthe text you feel is needed before adding the gallery. All images you want in the gallery need to be included in the header after the `gallery:` tag. Finally, you then include the gallery in the body of the file like so:

```
{% include gallery  %}
```


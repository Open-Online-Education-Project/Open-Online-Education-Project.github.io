# Open-Online-Education-Project.github.io

This repository contains the pages for the [ooep.org](https://ooep.org) website.  Styles, templates, and branding are in [Open-Online-Education-Project/OOEP-Jekyll-Theme](https://github.com/Open-Online-Education-Project/OOEP-Jekyll-Theme).

## Creating and Editing Pages

Jekyll, which we are using to host our website, supports Markdown (kramdown specifically).  See [the CommonMark website](https://commonmark.org/help/) for a tutorial.  However, just creating a Markdown file isn't enough.  Jekyll requires a particular sort of page header, which it calls [_front matter_](https://jekyllrb.com/docs/front-matter/), to tell it how to treat the files, and anything without that header will just be treated as a raw file for download.

A file with front matter looks like this:
```
---
layout: page
title: My Sweet Page
---
[content goes here]
```

The front matter consists of three dashes, a list of options, and then three dashes again.

| Front matter option | Required? | Defined By | Description |
| --- | --- | --- | --- |
| `layout` | Yes | Jekyll | Loosely, the type of page this is.  Specifically, the template that Jekyll will use to render your page.  Our theme defines several types of templates; see below for more. |
| `title` | Yes | Jekyll | The title of the page. |
| `permalink` | No, and not recommended | Jekyll | By default, the name of the page file (`contact.md`, say) defines the URL (`ooep.org/contact`).  This option lets you set another URL (`permalink: /contact-us/` gives `ooep.org/contact-us`) without changing the filename. |
| `published` | No | Jekyll | Setting this to `false` means that Jekyll will not include your page in the published site.  This can be useful for work-in-progress pages that you still want to commit to GitHub. |
| `nav_title` | No | The OOEP theme | If you want your page to show up in the navigation bar at the top of the website, set this option to the name you want to give it there. |
| `nav_order` | If you have `nav_title` | The OOEP theme | The position of your page in the navigation bar.  Lower numbers come first.  The home page (`index.md`), for instance, has `nav_order: 1`. |

## Layouts

Currently, the OOEP theme supports two kinds of layouts.

### `layout: page`
The standard website page.  It will automatically fill in a header, navigation, branding, styling, and everything else you need.  Just write the text of the page in Markdown.  You can also use pure HTML if you want, although you'll still need the front matter.  In this case, don't write a full web page.  Just write the HTML that would go in the content section.  The template will embed it into the standard HTML template for you.

### `layout: redirect`
A way to redirect the user outside the website.  Redirect pages must have file extension `.html` and must look like this:

```
---
layout: redirect
[Rest of front matter, including possibly nav_title]
---
[URL of page to redirect to]
```

If we were ever to have a blog, we would have a `post` layout as well.

### Redirect Link Scroll: 

The following is a list of the different ooep hotlinks. That is, change one of these hotlinks in the jekyll to have ooep.org/link redirect there. In the future some of these may turn into non-hotlinks and thus linking to ooep.org/link is ideal. 

* General OOEP Related
  * jobs: Google doc for job listing across all OOEP matters. 
  * signup: Google form for signing up for an OOEP job. 

* OCMI Related
  * OCMIAtHarvard: OCMI Harvard letter that we collect faculty signatures for. 
  * OCMIAtHarvardForm: Google form for sign ons from faculty
  * OCMIFAQ: Frequently asked questions of faculty 

* Open edTech Community Related
  * projects: list of the open-source development projects under 
  * projectagreement: Link to a view of the project agreement 
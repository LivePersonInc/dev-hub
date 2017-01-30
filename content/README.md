# LivePerson API Documentation repository

## How to...
### Add Section or pages
* Add your product to the [sidebar](_data/sidebars/home_sidebar.yml)
* Add your page under the [pages](pages) directory. Each section pages should be put under separate folder.
* Include in your markdown page file Jekyll ``Front Matter`` (see below)
* Add you images to the [img](img) directory.


## SideBar

The sidebar is defined using YAML file like this:

```yml
entries:
- title: Sidebar
  product: product
  folders:
  - title: Common Guidlines
    output: web
    subfolders:
    - title: Introduction
      output: web
      folderitems:
      - title: Home
        url: /not_yet.html
        output: web
    - title: Services Domains
      output: web
      folderitems:
      - title: Home
        url: /not_yet.html
        output: web

```
## FrontMatter
Front matter is a header in the markdown files that guides Jekyll how to render the page.

```
---
title: Tutorials
permalink: /consumer-int-tutorials.html
toc: false/true
keywords: add here keywords to be included in the search
---

Put here your markdown
```

The ``permalink`` should contain filename with html suffix. Refer to this ``permalink`` in the sidebar. In order not to break page name uniqness add the section as prefix to the permalink.

## For other Options

Please refer to the theme documentation here: [http://idratherbewriting.com/documentation-theme-jekyll/](http://idratherbewriting.com/documentation-theme-jekyll/)

## Building the site locally

You can test and review your changes locally. (Tested with mac, and Docker version 1.12.3, build 6b644ec).

```sh
~ docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll \
  -it -p 127.0.0.1:4005:4005 jekyll/jekyll bundle exec jekyll serve --watch
```

It will take a few minutes for docker to install in your container the needed ruby gems. In the end you should see something like:

```sh
                    done in 22.098 seconds.
 Auto-regeneration: enabled for '/srv/jekyll'
Configuration file: /srv/jekyll/_config.yml
    Server address: http://0.0.0.0:4005/
  Server running... press ctrl-c to stop.
```

Then open the browser in the specified ``Server address`` (http://0.0.0.0:4005/).
Keep this process running whe you make changes in the files.


### Build the site in your forked github pages

Another way is to commit your changes to your forked repository, wait a minute and then go to: https://lpgithub.dev.lprnd.net/pages/__YOUR_USERNAME__/__YOUR_FORKED_REPO_NAME__.

In this way you will not see the logs, errors and warnings of jekyll while building your pages.


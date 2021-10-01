---
title: jekyll-redirect-html
layout: splash
header:
  overlay_image: /assets/images/unsplash.jpg
  overlay_filter: 0.25
  actions:
    - label: "<i class='fas fa-download'></i> Install now"
      url: "#installation"
    - label: "<i class='fab fa-github'></i> View on GitHub"
      url: "https://github.com/jsware/jekyll-redirect-html"
  caption: "Photo credit: [**Unsplash**](https://unsplash.com/photos/C7B-ExXpOIE)"
excerpt: >
  A Jekyll layout that redirects to a new page without using the
  jekyll-redirect-from plugin.
---
For some Jekyll sites, setting up URL re-writes or HTTP 301 Moved Permanently response codes on HTTP web servers (such as Apache or NGINX) is not possible. If you reorganise your site, external links to your original pages will be broken, which is not a great web experience.

The redirect layout creates an HTML redirection page from the original page URL to its new location.

## Installation

1. Copy the `_layouts/redirection.html` file to your Jekyll `_layouts` folder.
1. Optionally create a `_redirects` folder, adding it to the `include:` section of your `_config.yml`.
1. Create a page with the front matter below. The redirect file name is not important as the original and redirect page URLs are controlled by `permalink` and `redirect` front matter settings.

## Redirect Page
```yaml
---
layout: redirection
permalink: /path/to/original/page/
redirect: /path/to/correct/page/
---
```

**NB: The layout has been renamed from `redirect.html` to `redirection.html` to avoid interference with [jekyll-redirect-from](https://github.com/jekyll/jekyll-redirect-from) plugin.**
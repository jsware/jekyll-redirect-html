# jekyll-redirect-html
A Jekyll layout that redirects to a new page.

For some Jekyll sites, setting up URL re-writes or HTTP 301 Moved Permanently response codes on HTTP web servers (such as Apache or NGINX) is not possible. If you reorganise your site, external links to your original pages will be broken, which is not a great web experience.

The redirect layout creates an HTML redirection page from the original page URL to its new location.

## Installation

1. Copy the `_layouts/redirect.html` file to your Jekyll `_layouts` folder.
1. Optionally create a `_redirects` folder, adding it to the `include:` section of your `_config.yml`.
1. Create a page with the front matter below. The redirect file name is not important as the original and redirect page URLs are controlled by `permalink` and `redirect` front matter settings.

## Redirect Page
```yaml
---
layout: redirect
permalink: /path/to/original/page/
redirect: /path/to/correct/page/
---
```

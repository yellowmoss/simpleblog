# Minimal Jeckyll Template

This is a minimal setup of a jekyll static site blog 
using some liquid syntax, markdown and css. No javascript.

It's main purpose is to be used as a DIY baseline blog 
structure from which to customise.

I can think of ways to improve it with keyword metadata 
or even json-ld

The blog is here:

https://yellowmoss.github.io/simpleblog/

IMPROVEMENTS

Take the repository name out of the default.html layout


### Liquid syntax

#### Filter

{{ input | function: arg }}

{{ "Text" | append: "My Blog" }} 

#### Loop

{% for post in site.posts %}

`<a href="{{ post.url | relative_url }}">{{ post.title }}</a>`

{% endfor %}

#### Variables

* page.title
* page.layout
* page.content
* page.title
* page.url
* page.date
* page.categories
* page.tags
* page.slug

* page.custom_var

as defined in: _config.yaml

* site.title
* site.baseurl
* site.url
* site description

* site.posts (blog posts)
* site.pages (standalone pages)
* site.data.filename.key (accesses key in _data/filename.yaml)
* site.collections

##### Filters
relative_url

Usage: {{ '/assets/style.css' | relative_url }}

ensures your URL is relative to the site's root, respecting the baseurl configuration.

absolute_url

Usage: {{ '/assets/style.css' | absolute_url }}

prepends site.url as well as site.baseurl to create a full, absolute URL.

layout Variables (layout.):

When processing a layout file, it has access to its own front matter variables via the layout object.

include Variables (include.):

Inside an included file (from the _includes directory),

any variables passed to the include are accessed via the include object.

Usage (inside _includes/my_include.html if called with

{% include my_include.html title="Hello" %}): {{ include.title }}

forloop Variables:

When you are inside a {% for ... in ... %} loop, helper variables like forloop.index,

forloop.first, and forloop.last are available for controlling iteration.

Essays with margin notes.
Built with [Zola](https://www.getzola.org).

## Develop

```sh
zola serve
```

Opens <http://127.0.0.1:1111> with live reload.

## Build

```sh
zola build
```

Output lands in `public/`.

## Writing

Posts live in `content/posts/*.md`.
Each post needs TOML frontmatter:

```md
+++
title = "The title"
date = 2026-04-16

[taxonomies]
tags = ["rust"]
+++

Body goes here.
```

### Asides

Use the `aside` shortcode anywhere in a post:

```md
The interpreter walks the AST node by node.

{% aside() %}
Tree-walking is slow but easy to reason about.
Bob Nystrom builds one in Part II before switching to bytecode.
{% end %}

Each node dispatches on its type...
```

On wide screens the aside floats into the right margin.
On narrow screens it becomes an inline callout.

## Layout

```
config.toml               site config (base url, taxonomies, markdown opts)
content/
  _index.md               home page
  posts/
    _index.md             section index
    *.md                  posts
templates/
  base.html               shared chrome
  index.html              home
  section.html            posts list
  page.html               single post
  shortcodes/
    aside.html            margin note
sass/
  main.scss               typography + layout
```

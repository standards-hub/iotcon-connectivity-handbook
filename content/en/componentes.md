---
title: Componentes
description: 'Install @nuxt/content in only two steps in your Nuxt project.'
category: Getting started
position: 2
multiselectOptions:
  - VuePress
  - Gridsome
  - Nuxt
---

## CodeGroup

<code-group>
  <code-block label="Yarn" active>

  ```bash
  yarn add @nuxt/content
  ```

  </code-block>
  <code-block label="NPM">

  ```bash
  npm install @nuxt/content
  ```

  </code-block>
</code-group>


```js[nuxt.config.js]
{
  modules: [
    '@nuxt/content'
  ],
  content: {
    // Options
  }
}
```

## Code - Script


**tsconfig.json**

```json
{
  "compilerOptions": {
    "types": [
      "@nuxt/types",
      "@nuxt/content"
    ]
  }
}
```
### Code - Html


```md[home.md]
# Lorem ipsum
## dolor—sit—amet
### consectetur &amp; adipisicing
#### elit
##### elit
```

```html
<h1 id="lorem-ipsum-"><a href="#lorem-ipsum-" aria-hidden="true" tabindex="-1"><span class="icon icon-link"></span></a>Lorem ipsum</h1>
<h2 id="dolorsitamet"><a href="#dolorsitamet" aria-hidden="true" tabindex="-1"><span class="icon icon-link"></span></a>dolor—sit—amet</h2>
<h3 id="consectetur--adipisicing"><a href="#consectetur--adipisicing" aria-hidden="true" tabindex="-1"><span class="icon icon-link"></span></a>consectetur &#x26; adipisicing</h3>
<h4 id="elit"><a href="#elit" aria-hidden="true" tabindex="-1"><span class="icon icon-link"></span></a>elit</h4>
<h5 id="elit-1"><a href="#elit-1" aria-hidden="true" tabindex="-1"><span class="icon icon-link"></span></a>elit</h5>
```
### Code - Front Matter

```md
---
title: Introduction
description: Learn how to use @nuxt/content.
---
```

These variables will be injected into the document:

```json
{
  body: Object
  excerpt: Object
  title: "Introduction"
  description: "Learn how to use @nuxt/content."
  dir: "/"
  extension: ".md"
  path: "/index"
  slug: "index"
  toc: Array
  createdAt: DateTime
  updatedAt: DateTime
}
```

## Comentario
> **Why?**
>
> Because of the way nuxt works the `$content` property on the context has to be merged into the nuxt `Context` interface via [declaration merging](https://www.typescriptlang.org/docs/handbook/declaration-merging.html). Adding `@nuxt/content` to your types will import the types from the package and make typescript aware of the additions to the `Context` interface.

> You can check the [basic syntax guide](https://www.markdownguide.org/basic-syntax) to help you master Markdown


## Properties
This module will parse `.md`, `.yaml`, `.yml`, `.csv`, `.json`, `.json5`, `.xml` files and generate the following properties:

- `dir`
- `path`
- `slug`
- `extension` (ex: `.md`)
- `createdAt`
- `updatedAt`



### Alertas

<alert type="info">
Be careful to enter <code>&lt;!--more--&gt;</code> exactly; i.e., all lowercase and with no whitespace.
</alert>

<alert type="warning">

An issue exists with locally registered components and live edit in development, since **v1.5.0** you can disable it by setting `liveEdit: false` (see [configuration](/configuration#liveedit)).

</alert>




---
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
title: Programá tus slides con Slidev
info: 10Pines Conf 2025 - Jess
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
seoMeta:
  # By default, Slidev will use ./og-image.png if it exists,
  # or generate one from the first slide if not found.
  ogImage: auto
  # ogImage: https://cover.sli.dev
---

# **Programá tus slides**
## *usando Slidev*

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

---
layout: image-right
image: https://pbs.twimg.com/media/GQBCg1zWEAAyVwV?format=jpg&name=large
transition: slide-left
---

# <span v-mark.highlight.yellow>Anthony Fu</span>

Creador de Slidev

<div class="mt-16 flex flex-col gap-lg">
  <div>
    Working at <a href="https://nuxtlabs.com" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/nuxtlabs.png')"></span>NuxtLabs</a> / <a href="https://vercel.com" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/vercel.png')"></span>Vercel</a>
  </div>
  <div>
    Creator of <a href="https://github.com/vitest-dev/vitest" class="markdown-magic-link  " target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/vitest-dev.png');"></span>Vitest</a> <a href="https://github.com/slidevjs/slidev" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/slidevjs.png')"></span>Slidev</a> <a href="https://github.com/vueuse/vueuse" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/vueuse.png');"></span>VueUse</a> <a href="https://github.com/unocss/unocss" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/unocss.png');"></span>UnoCSS</a> <a href="https://github.com/elk-zone/elk" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/elk-zone.png');"></span>Elk</a> <a href="https://github.com/type-challenges/type-challenges" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/type-challenges.png');"></span>Type Challenges</a>
  </div>
  <div>
    Core team of <a href="https://github.com/vuejs/core" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://vuejs.org/logo.svg');"></span>Vue</a> <a href="https://github.com/nuxt/nuxt" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://nuxt.com/assets/design-kit/icon-green.svg');"></span>Nuxt</a> <a href="https://github.com/vitejs/vite" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://vitejs.dev/logo.svg');"></span>Vite</a>
  </div>
  <div>
    Maintaining <a href="https://github.com/shikijs/shiki" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/shikijs.png');"></span>Shiki</a> <a href="https://github.com/twoslashes/twoslash" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/twoslashes.png');"></span>Twoslash</a> <a href="https://github.com/eslint-stylistic/eslint-stylistic" class="markdown-magic-link" target="_blank" rel="noopener"><span class="markdown-magic-link-image" style="background-image: url('https://github.com/eslint-stylistic.png');"></span>ESLint Stylistic</a>
  </div>
</div>

<div class="face">
  <span v-mark.circle.yellow="{at: 1, strokeWidth: 10 }"></span>
</div>

<style>
.face {
  left: 59%;
  position: absolute;
  top: 18%;
}

.face span {
  display: block;
  height: 150px;
  width: 150px;
}

.markdown-magic-link {
    display: inline-flex;
    align-items: center;
    transform: translateY(3px);
    line-height: 100%;
    color: #686868;
    background: rgba(136, 136, 136, 0.133);
    gap: 0.25rem;
    border-radius: 0.25rem;
    padding: 0.25rem 0.375rem;
    border-width: 0 !important;
    font-size: 0.85em;
}

.markdown-magic-link:hover {
    color: #454545;
    background: rgba(136, 136, 136, 0.2);
}

.markdown-magic-link-image {
    display: inline-block;
    height: 1.1em;
    width: 1.1em;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    border-radius: 2px;
}
</style>

---
layout: default
---

# Instalación de proyecto

::code-group

```sh [pnpm]
# If you haven't installed pnpm
npm i -g pnpm

pnpm create slidev
```

```sh [npm]
# Not recommended -
# NPM will download the packages each time you create a new project,
# which is slow and takes up a lot of space

npm init slidev@latest
```

```sh [yarn]
yarn create slidev
```

```sh [bun]
bun create slidev
```

```sh [deno]
deno init --npm slidev
```

::

---
layout: two-cols
layoutClass: gap-3xl
---

# Frontmatter

Es una forma de identificar metadata en archivos markdown, generalmente se utiliza el formato YAML

```md [slides.md]
---
title: "Mi título"
description: "Descripción"
tags:
    - JavaScript
    - Markdown
---

# Título de mi sección

Contenido de mi archivo
```

::right::

<div v-click>
  <LightOrDark width="100" alt="astro logo">
    <template #dark="props">
      <img src="https://astro.build/assets/press/astro-logo-light.png" v-bind="props"/>
    </template>
    <template #light="props">
      <img src="https://astro.build/assets/press/astro-logo-dark.svg" v-bind="props"/>
    </template>
  </LightOrDark>
</div>

<img v-click src="https://images.icon-icons.com/2699/PNG/512/docusaurus_logo_icon_171229.png" alt="docusaurus logo">

<div v-click>
  <LightOrDark width="100" alt="jekyll logo">
    <template #dark="props">
      <img src="https://happycoding.io/tutorials/html/images/jekyll-6.png" v-bind="props"/>
    </template>
    <template #light="props">
      <img src="https://nelbren.com/assets/images/posts/jekyll-logo.png" v-bind="props"/>
    </template>
  </LightOrDark>
</div>

<style>
.slidev-layout {
  grid-template-columns: 3fr 2fr;
}
</style>

---
transition: slide-up
---

<<< @/snippets/initial-frontmatter.md {all|1-2|3-5|6-11|12-13}{lines: true}


---
layout: two-cols
transition: slide-down
layoutClass: gap-3xl
---

# UnoCSS

Engine para generar Atomic CSS

Fuertemente inspirado en Windi CSS (a su vez autoproclamado como _"la alternativa on-demand a Tailwind"_)

La forma tradicional de construir Atomic CSS es proveer todas las utility classes que puedas llegar a necesitar con un preprocesador, por ejemplo:

````md magic-move {lines: false}

```scss
// style.scss

@for $i from 1 through 10 {
  .m-#{$i} {
    margin: $i / 4 rem;
  }
}
```

```scss
.m-1 { margin: 0.25 rem; }
.m-2 { margin: 0.5 rem; }
.m-3 { margin: 0.75 rem; }
.m-4 { margin: 1 rem; }
.m-5 { margin: 1.25 rem; }
.m-6 { margin: 1.5 rem; }
.m-7 { margin: 1.75 rem; }
.m-8 { margin: 2 rem; }
.m-9 { margin: 2.25 rem; }
.m-10 { margin: 2.5 rem; }
```

````

::right::

::div{v-click}
<span class="rotor"><twemoji-thinking-face v-motion /></span> ¿Y si queremos otros aliases como `mt` para `margin-top` y `mb` para `margin-bottom`? ¿O implementar variantes con `:hover` y `:focus`?
::

::div{v-click class="my-4"}
Para combatir los MBs de CSS generados, Tailwind llegó a la solución de usar [PurgeCSS](https://purgecss.com/) para escanear el bundle y remover las reglas que no estás usando
::

<img class="my-8" v-after src="https://antfu.me/images/unocss-traditional-way.png" />

::div{v-click}
En cambio, la forma "on demand" invierte el orden de estos pasos y hace un pre-escaneo del código
::

<style>
@keyframes spinAlternate {
  from {
  transform: rotate(-50deg);
  }
  to {
    transform: rotate(50deg);
  }
}

.rotor {
  display: inline-block;
  animation: spinAlternate 1s linear infinite alternate;
}
</style>

---
transition: slide-up
---

<<< @/snippets/initial-frontmatter.md {14-16|17-18|19-20}{lines: true}

---
transition: slide-down
---

# Vue component syntax vs MDC syntax

<div grid="~ cols-2 gap-col-4xl gap-row-sm" m="t-2">

```vue-html
<Card type="idea">
  This is the title

  <template #content>
    I'm some _cool_ **content**
  </template>
</Card>
```

```mdc
::card{type="warning"}
  This is the title

  #content
  I'm some _cool_ **content**
::
```

<Card type="idea">
  This is the title

  <template #content>
    I'm some _cool_ **content**
  </template>
</Card>

::card{type="warning"}
  This is the title

  #content
  I'm some _cool_ **content**
::

</div>

---
transition: slide-left
---

<<< @/snippets/initial-frontmatter.md {22-26}{lines: true}

---
transition: fade-out
---

# Soporte para LaTeX

$$ {1|3|all}
\begin{aligned}
\nabla \cdot \vec{E} &= \frac{\rho}{\varepsilon_0} \\
\nabla \cdot \vec{B} &= 0 \\
\nabla \times \vec{E} &= -\frac{\partial\vec{B}}{\partial t} \\
\nabla \times \vec{B} &= \mu_0\vec{J} + \mu_0\varepsilon_0\frac{\partial\vec{E}}{\partial t}
\end{aligned}
$$

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---
transition: slide-up
level: 2
---

# Navigation

Hover on the bottom-left corner to see the navigation's controls panel, [learn more](https://sli.dev/guide/ui#navigation-bar)

## Keyboard Shortcuts

|                                                     |                             |
| --------------------------------------------------- | --------------------------- |
| <kbd>right</kbd> / <kbd>space</kbd>                 | next animation or slide     |
| <kbd>left</kbd>  / <kbd>shift</kbd><kbd>space</kbd> | previous animation or slide |
| <kbd>up</kbd>                                       | previous slide              |
| <kbd>down</kbd>                                     | next slide                  |

<!-- https://sli.dev/guide/animations.html#click-animation -->
<img
  v-click
  class="absolute -bottom-9 -left-7 w-80 opacity-50"
  src="https://sli.dev/assets/arrow-bottom-left.svg"
  alt=""
/>
<p v-after class="absolute bottom-23 left-45 opacity-30 transform -rotate-10">Here!</p>

---
layout: two-cols
layoutClass: gap-16
---

# Table of contents

You can use the `Toc` component to generate a table of contents for your slides:

```html
<Toc minDepth="1" maxDepth="1" />
```

The title will be inferred from your slide content, or you can override it with `title` and `level` in your frontmatter.

::right::

<Toc text-sm minDepth="1" maxDepth="2" />

---
layout: image-right
image: https://cover.sli.dev
---

# Code

Use code snippets and get the highlighting directly, and even types hover!

```ts [filename-example.ts] {all|4|6|6-7|9|all} twoslash
// TwoSlash enables TypeScript hover information
// and errors in markdown code blocks
// More at https://shiki.style/packages/twoslash
import { computed, ref } from 'vue'

const count = ref(0)
const doubled = computed(() => count.value * 2)

doubled.value = 2
```

<arrow v-click="[4, 5]" x1="350" y1="310" x2="195" y2="342" color="#953" width="2" arrowSize="1" />

<!-- This allow you to embed external code blocks -->
<<< @/snippets/external.ts#snippet

<!-- Footer -->

[Learn more](https://sli.dev/features/line-highlighting)

<!-- Inline style -->
<style>
.footnotes-sep {
  @apply mt-5 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

<!--
Notes can also sync with clicks

[click] This will be highlighted after the first click

[click] Highlighted with `count = ref(0)`

[click:3] Last click (skip two clicks)
-->

---
level: 2
---

# Shiki Magic Movesss

Powered by [shiki-magic-move](https://shiki-magic-move.netlify.app/), Slidev supports animations across multiple code snippets.

Add multiple code blocks and wrap them with <code>````md magic-move</code> (four backticks) to enable the magic move. For example:

````md magic-move {lines: true}
```ts {*|2|*}
// step 1
const author = reactive({
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery'
  ]
})
```

```ts {*|1-2|3-4|3-4,8}
// step 2
export default {
  data() {
    return {
      author: {
        name: 'John Doe',
        books: [
          'Vue 2 - Advanced Guide',
          'Vue 3 - Basic Guide',
          'Vue 4 - The Mystery'
        ]
      }
    }
  }
}
```

```ts
// step 3
export default {
  data: () => ({
    author: {
      name: 'John Doe',
      books: [
        'Vue 2 - Advanced Guide',
        'Vue 3 - Basic Guide',
        'Vue 4 - The Mystery'
      ]
    }
  })
}
```

Non-code blocks are ignored.

```vue
<!-- step 4 -->
<script setup>
const author = {
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery'
  ]
}
</script>
```
````

---

# Components

<div grid="~ cols-2 gap-4">
<div>

You can use Vue components directly inside your slides.

We have provided a few built-in components like `<Tweet/>` and `<Youtube/>` that you can use directly. And adding your custom components is also super easy.

```html
<Counter :count="10" />
```

<!-- ./components/Counter.vue -->
<Counter :count="10" m="t-4" />

Check out [the guides](https://sli.dev/builtin/components.html) for more.

</div>
<div>

```html
<Tweet id="1390115482657726468" />
```

<Tweet id="1390115482657726468" scale="0.65" />

</div>
</div>

<!--
Presenter note with **bold**, *italic*, and ~~striked~~ text.

Also, HTML elements are valid:
<div class="flex w-full">
  <span style="flex-grow: 1;">Left content</span>
  <span>Right content</span>
</div>
-->

---
class: px-20
---

# Themes

Slidev comes with powerful theming support. Themes can provide styles, layouts, components, or even configurations for tools. Switching between themes by just **one edit** in your frontmatter:

<div grid="~ cols-2 gap-2" m="t-2">

```yaml
---
theme: default
---
```

```yaml
---
theme: seriph
---
```

<img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-default/01.png?raw=true" alt="">

<img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-seriph/01.png?raw=true" alt="">

</div>

Read more about [How to use a theme](https://sli.dev/guide/theme-addon#use-theme) and
check out the [Awesome Themes Gallery](https://sli.dev/resources/theme-gallery).

---

# Clicks Animations

You can add `v-click` to elements to add a click animation.

<div v-click>

This shows up when you click the slide:

```html
<div v-click>This shows up when you click the slide.</div>
```

</div>

<br>

<v-click>

The <span v-mark.red="3"><code>v-mark</code> directive</span>
also allows you to add
<span v-mark.circle.orange="4">inline marks</span>
, powered by [Rough Notation](https://roughnotation.com/):

```html
<span v-mark.underline.orange>inline markers</span>
```

</v-click>

<div mt-20 v-click>

[Learn more](https://sli.dev/guide/animations#click-animation)

</div>

---

# Motions

Motion animations are powered by [@vueuse/motion](https://motion.vueuse.org/), triggered by `v-motion` directive.

```html
<div
  v-motion
  :initial="{ x: -80 }"
  :enter="{ x: 0 }"
  :click-3="{ x: 80 }"
  :leave="{ x: 1000 }"
>
  Slidev
</div>
```

<div class="w-60 relative">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute inset-0"
      src="https://sli.dev/logo-square.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :enter="final"
      class="absolute inset-0"
      src="https://sli.dev/logo-circle.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final"
      class="absolute inset-0"
      src="https://sli.dev/logo-triangle.png"
      alt=""
    />
  </div>

  <div
    class="text-5xl absolute top-14 left-40 text-[#2B90B6] -z-1"
    v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    Slidev
  </div>
</div>

<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<div
  v-motion
  :initial="{ x:35, y: 30, opacity: 0}"
  :enter="{ y: 0, opacity: 1, transition: { delay: 3500 } }">

[Learn more](https://sli.dev/guide/animations.html#motion)

</div>

---

# LaTeX

LaTeX is supported out-of-box. Powered by [KaTeX](https://katex.org/).

<div h-3 />

Inline $\sqrt{3x-1}+(1+x)^2$

Block
$$ {1|3|all}
\begin{aligned}
\nabla \cdot \vec{E} &= \frac{\rho}{\varepsilon_0} \\
\nabla \cdot \vec{B} &= 0 \\
\nabla \times \vec{E} &= -\frac{\partial\vec{B}}{\partial t} \\
\nabla \times \vec{B} &= \mu_0\vec{J} + \mu_0\varepsilon_0\frac{\partial\vec{E}}{\partial t}
\end{aligned}
$$

[Learn more](https://sli.dev/features/latex)

---

# Diagrams

You can create diagrams / graphs from textual descriptions, directly in your Markdown.

<div class="grid grid-cols-4 gap-5 pt-4 -mb-6">

```mermaid {scale: 0.5, alt: 'A simple sequence diagram'}
sequenceDiagram
    Alice->John: Hello John, how are you?
    Note over Alice,John: A typical interaction
```

```mermaid {theme: 'neutral', scale: 0.8}
graph TD
B[Text] --> C{Decision}
C -->|One| D[Result 1]
C -->|Two| E[Result 2]
```

```mermaid
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
```

```plantuml {scale: 0.7}
@startuml

package "Some Group" {
  HTTP - [First Component]
  [Another Component]
}

node "Other Groups" {
  FTP - [Second Component]
  [First Component] --> FTP
}

cloud {
  [Example 1]
}

database "MySql" {
  folder "This is my folder" {
    [Folder 3]
  }
  frame "Foo" {
    [Frame 4]
  }
}

[Another Component] --> [Example 1]
[Example 1] --> [Folder 3]
[Folder 3] --> [Frame 4]

@enduml
```

</div>

Learn more: [Mermaid Diagrams](https://sli.dev/features/mermaid) and [PlantUML Diagrams](https://sli.dev/features/plantuml)

---
foo: bar
dragPos:
  square: 691,32,167,_,-16
---

# Draggable Elements

Double-click on the draggable elements to edit their positions.

<br>

###### Directive Usage

```md
<img v-drag="'square'" src="https://sli.dev/logo.png">
```

<br>

###### Component Usage

```md
<v-drag text-3xl>
  <div class="i-carbon:arrow-up" />
  Use the `v-drag` component to have a draggable container!
</v-drag>
```

<v-drag pos="663,206,261,_,-15">
  <div text-center text-3xl border border-main rounded>
    Double-click me!
  </div>
</v-drag>

<img v-drag="'square'" src="https://sli.dev/logo.png">

###### Draggable Arrow

```md
<v-drag-arrow two-way />
```

<v-drag-arrow pos="67,452,253,46" two-way op70 />

---
src: ./pages/imported-slides.md
hide: false
---

---

# Monaco Editor

Slidev provides built-in Monaco Editor support.

Add `{monaco}` to the code block to turn it into an editor:

```ts {monaco}
import { ref } from 'vue'
import { emptyArray } from './external'

const arr = ref(emptyArray(10))
```

Use `{monaco-run}` to create an editor that can execute the code directly in the slide:

```ts {monaco-run}
import { version } from 'vue'
import { emptyArray, sayHello } from './external'

sayHello()
console.log(`vue ${version}`)
console.log(emptyArray<number>(10).reduce(fib => [...fib, fib.at(-1)! + fib.at(-2)!], [1, 1]))
```

---
layout: center
class: text-center
---

# Learn More

[Documentation](https://sli.dev) · [GitHub](https://github.com/slidevjs/slidev) · [Showcases](https://sli.dev/resources/showcases)

<PoweredBySlidev mt-10 />

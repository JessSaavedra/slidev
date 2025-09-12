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
layout: two-cols
layoutClass: gap-3xl items-center
---

# Cómo empezar

::div{ class="mb-4" }
> Requiere <a href="https://nodejs.org" target="_blank" rel="noreferrer">Node.js</a> &gt;= 18.0 instalado
::

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

::right::

# Tecnologías

- [Vite](https://vitejs.dev/)
- [Vue 3](https://v3.vuejs.org/) (con soporte para [Markdown](https://daringfireball.net/projects/markdown/syntax))
- [UnoCSS](https://github.com/unocss/unocss)
- Muchas integraciones para soportar funcionalidades copadas <twemoji-grinning-face />

---
layout: default
---

# Cómo funciona

```mermaid {scale: 0.55}
%%{init: { 'themeVariables': { 'fontSize': '20px' } } }%%
flowchart LR
    n1["slides.md"]
    B[<u>**#64;slidev/parser**</u><br>- dividir slides <br>- manipular frontmatter<br>- detectar &lt;v-click&gt;]
    C[<u>**markdown-it**</u><br>- parsear markdown<br>- convertirlo en tokens HTML]
    D[<u>**vite-plugin-md**</u><br>- wrappearlos en Vue SFC<br>- exportar componentes .vue]
    E[<u>**Vite + Vue compiler**</u><br>- compilar Vue SFC a JS<br>- bundling + HMR]
    n2["Vue en el navegador"]
    classDef default stroke-width:3px;
    classDef none stroke-width:0,fill:none;
    class n1 none;
    class n2 none;

    n1 e1@==> B e2@==> C e3@==> D e4@==> E e5@==> n2
    n1@{ img: "https://images.emojiterra.com/twitter/v13.1/512px/1f4c4.png", h: 80, w: 80, pos: "b", constraint: "on" }
    n2@{ img: "https://em-content.zobj.net/source/skype/289/desktop-computer_1f5a5-fe0f.png", h: 80, w: 80, pos: "b", constraint: "on" }
    e1@{ animate: true }
    e2@{ animate: true }
    e3@{ animate: true }
    e4@{ animate: true }
    e5@{ animate: true }
```

<style>
h1 {
    margin-bottom: 140px;
}
</style>

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

# Frontmatter inicial

<<< @/snippets/initial-frontmatter.md {all|1-2|3-5|6-11|12-13}{lines: true, maxHeight: '400px'}


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

# Frontmatter inicial

<<< @/snippets/initial-frontmatter.md {14-16|17-18|19-20}{lines: true, maxHeight: '400px'}

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

# Frontmatter inicial

<<< @/snippets/initial-frontmatter.md {none|21-26}{lines: true, maxHeight: '400px'}

---
layout: two-cols-header
layoutClass: gap-3xl
---

# Componentes built-in

::left::

###### Un tweet interactivo
<Tweet id="1392246507793915904" scale="0.7" />

::right::

###### Un contador (?){v-click}
<Counter :count="10" m="t-2 b-6" v-after />


###### Un reproductor de video{v-click}

<SlidevVideo controls v-after m="t-2">
    <source src="" type="video/webm" />
</SlidevVideo>

<style>
.slidev-layout {
    grid-template-columns: 1fr 2fr;
}
</style>

---

# Soporte para LaTeX

<div h-3/>

inline... $\sqrt{3x-1}+(1+x)^2$

...y en bloque <twemoji-astonished-face/>

$$ {all|1|2|3}
\begin{aligned}
\nabla \cdot \vec{E} &= \frac{\rho}{\varepsilon_0} \\
\nabla \cdot \vec{B} &= 0 \\
\nabla \times \vec{E} &= -\frac{\partial\vec{B}}{\partial t} \\
\nabla \times \vec{B} &= \mu_0\vec{J} + \mu_0\varepsilon_0\frac{\partial\vec{E}}{\partial t}
\end{aligned}
$$

---
layout: image
image: https://pymstatic.com/125774/conversions/por-que-es-famosa-mona-lisa-wide_webp.webp
---

---

# Monaco Editor

```ts {monaco-run}
class Ave {
    #energia: number = 100;
    
    comer(gramosAlpiste: number) {
        this.#energia += gramosAlpiste;
    }
    
    volar(km: number) {
        this.#energia -= 10 * km;
    }
    
    energia(): number {
      return this.#energia;
    }
}

const pepita = new Ave();
pepita.comer();

console.log(pepita.energia());
```

---
clicks: 6
---

# Mi tier list

<img src="https://tiermaker.com/images/uploads/blobid1668114252696.png">

<v-drag pos="778,46,61,78" v-if="2 < $clicks">
    <div class="w-60 relative">
        <div class="relative w-40 h-40">
            <img
                v-motion
                :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
                :enter="final"
                class="absolute inset-0"
                style="width: 50px"
                src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1e/Google_Slides_logo_%282014-2020%29.svg/1489px-Google_Slides_logo_%282014-2020%29.svg.png"
                alt="Google Slides logo"
            />
        </div>
    </div>
</v-drag>

<v-drag pos="736,43,97,93" v-if="0 < $clicks">
    <div class="w-60 relative">
        <div class="relative w-40 h-40">
            <img
                v-motion
                :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
                :enter="final"
                class="absolute inset-0"
                style="width: 90px"
                src="https://upload.wikimedia.org/wikipedia/commons/3/3b/Microsoft_PowerPoint_Logo.png"
                alt="Powerpoint logo"
            />
        </div>
    </div>
</v-drag>

<v-drag pos="742,49,84,83" v-if="1 < $clicks">
    <div class="w-60 relative">
        <div class="relative w-40 h-40">
            <img
                v-motion
                :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
                :enter="final"
                class="absolute inset-0"
                style="width: 80px"
                src="https://is1-ssl.mzstatic.com/image/thumb/Purple211/v4/f7/5d/bd/f75dbd29-3741-2af9-47d3-4bdaa79cfb5f/AppIcon-0-0-85-220-0-0-4-0-0-2x-0-0-0-0-0.png/1200x630bb.png"
                alt="Mac keynote logo"
            />
        </div>
    </div>
</v-drag>

<v-drag pos="762,33,83,83" v-if="4 < $clicks">
    <div class="w-60 relative">
        <div class="relative w-40 h-40">
            <img
                v-motion
                :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
                :enter="final"
                class="absolute inset-0"
                style="width: 80px"
                src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6a/Godot_icon.svg/2048px-Godot_icon.svg.png"
                alt="Godot logo"
            />
        </div>
    </div>
</v-drag>

<v-drag pos="762,43,84,81" v-if="3 < $clicks">
    <div class="w-60 relative">
        <div class="relative w-40 h-40">
            <img
                v-motion
                :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
                :enter="final"
                class="absolute inset-0"
                style="width: 70px"
                src="https://www.laborando.com.ar/wp-content/uploads/proyectordefilmina-e1727798514323.png"
                alt="Filminas"
            />
        </div>
    </div>
</v-drag>

<v-drag pos="707,8,124,128" v-if="5 < $clicks" style="scale: 0.5">
    <div class="w-40 relative">
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
    </div>
</v-drag>

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

---
layout: fact
class: text-center
---

# ¡Gracias!

¿Preguntas?

<PoweredBySlidev mt-10 />

<style>
.slidev-layout {
    background: url("https://cdn.jsdelivr.net/gh/slidevjs/slidev-covers@main/static/_eObctVlXn4.webp") no-repeat center center / cover;
}

.slidev-layout > div > span {
    background-color: #ffffffc7;
    padding: 0 0 0 .5em;
}
</style>

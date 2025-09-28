---
title: "Bloging using Asto.js and Github"
description: "Setting up the blogging using github CI/CD and Astro.js static site generation."
pubDate: "Aug 08 2024"
heroImage: "/portfolio_site/blog-placeholder-1.jpg"
---

Blogging is one of the simplest yet most powerful ways to share your thoughts, knowledge, and experiences with the world. Whether you want to document your learning journey, build a personal brand, or connect with a community, a blog acts as your digital home. Unlike fast-moving social media posts, blogs give your ideas a permanent place to live, where readers can revisit them anytime. With today’s tools, you don’t need to be a developer to start — you can set up a blog in minutes and focus on writing what truly matters.
<br><br>
Starting a blog today is easier than ever, but choosing the right tools can make all the difference and asto.js is perfect for the all static site generation.
<br><br>

<h1 class="md:text-3xl text-2xl font-bold"> Why choose Asto.js and Github</h1>

Astro is a modern **static site generator (SSG)** built for speed and simplicity.

In short: Astro helps you focus on **writing** instead of fighting with tooling.
<br><br>
Github: it is free and easy to host static sites direct from repository ¯\(ツ)/¯ not much thought went into it other than that.
<br><br>

<h1 class="md:text-3xl text-2xl font-bold"> Setting up Asto Project </h1>

**Prerequisites**

> Node.js - v18.20.8 or v20.3.0, v22.0.0 or higher. ( v19 and v21 are not supported.)

```bash
# create a new Astro project
npm create astro@latest my-blog
```

choose a blog template for easier configurations.

<br>

**Directories and Files**

Astro leverages an opinionated folder layout for your project. Every Astro project root should include the following directories and files:

**src/** - Your project source code (components, pages, styles, images, etc.)

**public/** - Your non-code, unprocessed assets (fonts, icons, etc.)

**content/** - Markdown files that has blog contents.

**package.json** - A project manifest.

**astro.config.mjs** - An Astro configuration file.

**tsconfig.json** - A TypeScript configuration file.

```text

    my-blog/
    ├── .github/
    │ └── workflows/
    │ └── deploy.yml
    ├── public/
    │ ├── favicon.ico
    │ └── robots.txt
    ├── src/
    │ ├── components/
    │ │ ├── Header.astro
    │ │ └── Footer.astro
    │ ├── content/
    │ │ └── blog/
    │ │ ├── first-post.md
    │ │ └── second-post.md
    │ ├── layouts/
    │ │ └── BlogLayout.astro
    │ ├── pages/
    │ │ ├── index.astro
    │ │ └── about.astro
    │ └── styles/
    │ └── main.css
    ├── astro.config.mjs
    ├── package.json
    ├── package-lock.json
    ├── tsconfig.json
    ├── .gitignore
    └── README.md
```

<br><br>

**Start the Astro dev server**

Start the Astro dev server to see the template blog site.

```bash
# run astro project
npm run dev
```

<br><br>

**Adding Tailwind Support**

In Astro >=5.2.0, use the astro add tailwind command for your package manager to install the official Vite Tailwind plugin. To add Tailwind 4 support to earlier versions of Astro, follow the instructions in the Tailwind docs to add the @tailwindcss/vite Vite plugin manually.

```bash
# add tailwind
npx astro add tailwind
```

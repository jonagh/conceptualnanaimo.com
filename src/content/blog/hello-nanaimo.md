---
title: 'Hello, Nanaimo!'
description: 'A test post to confirm heroImages are wired up correctly on the homepage grid and individual post pages.'
pubDate: 'May 17 2026'
heroImage: '../../assets/blog-placeholder-1.jpg'
---

Welcome to **Conceptual Nanaimo** — this is a test post to make sure everything is wired up correctly: the `heroImage` field in the content schema, the homepage post grid, and the individual blog post layout.

## What we're testing

1. **Schema** — the `heroImage` field in `content.config.ts` resolves the image path at build time using Astro's `image()` helper, giving you full type safety and optimised output.
2. **Homepage grid** — `src/pages/index.astro` fetches every post in the `blog` collection and renders each `heroImage` via Astro's `<Image>` component at `720×360`.
3. **Post page** — `src/layouts/BlogPost.astro` renders the `heroImage` as a full-width banner at `1020×510` above the article content.

## Writing a post with a heroImage

Add the `heroImage` field to your frontmatter pointing at a file inside `src/assets/`:

```
---
title: 'My Post'
description: 'A short description.'
pubDate: 'Jan 01 2027'
heroImage: '../../assets/my-photo.jpg'
---
```

Astro will process and optimise the image at build time — no manual resizing needed.

## Markdown works as expected

You can use all standard Markdown here: **bold**, _italic_, `inline code`, [links](https://astro.build), and more.

> Block quotes look like this.

And here is a short code block:

```js
const greeting = 'Hello, Nanaimo!';
console.log(greeting);
```

If everything looks right — a hero image at the top of this page, and a thumbnail card on the homepage — you're good to go.

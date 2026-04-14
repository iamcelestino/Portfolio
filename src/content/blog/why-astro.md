---
title: "Why I Rewrote My Site in Astro"
description: "A frank look at the tradeoffs of choosing a framework — and why static-first finally won me over."
pubDate: 2025-06-20
tags: ["dev", "astro", "performance", "tooling"]
---

My portfolio has been rebuilt seven times. React, Next.js, Gatsby, plain HTML, Svelte, Hugo, and now Astro. Each time, I told myself this was the last one.

I'm not naive enough to say that this time again. But I *am* willing to explain why Astro has made me happier than anything else.

## The Problem with JavaScript Frameworks for Content Sites

React is extraordinary. For highly interactive applications — dashboards, tools, anything with complex client state — it remains my first choice. But a portfolio site is not a complex interactive application.

It's text. Images. The occasional animation. A contact form.

Shipping 300KB of JavaScript to display my face and some words about what I do always felt like an architectural mismatch. Like driving a race car to the grocery store.


## What Astro Gets Right

Astro ships **zero JavaScript by default**. Components render to static HTML at build time. JavaScript is opt-in, only where interaction actually requires it.

This isn't a new idea — Hugo and Eleventy have done this for years. What Astro adds is the ability to use component frameworks (React, Svelte, Vue) in islands of interactivity when you need them, while keeping everything else static.

The mental model is clean. The output is fast. The developer experience is genuinely pleasant.

## The Numbers

Before Astro (Next.js): Lighthouse performance score of 71. First Contentful Paint: 2.3s.

After Astro: Lighthouse performance score of 99. First Contentful Paint: 0.4s.

Same content. Same design. Different architecture.

## The Tradeoffs

Astro isn't for everything. If your site is mostly application — authentication, real-time data, complex user state — Astro's model starts to fight you. The island architecture gets awkward when most of your page is an island.

But for portfolios, blogs, documentation, marketing sites? It's close to ideal.

I'll probably rebuild this site again someday. That's just who I am. But for now, I'm genuinely glad I chose Astro.

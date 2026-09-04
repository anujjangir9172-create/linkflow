# LinkFlow

A hero landing section built to spec: Vite + React 18 + TypeScript + Tailwind
CSS 3.4, with a canvas-based "boomerang" video background and CSS-only
(no Framer Motion) animations for the mobile nav.

This is a standalone project — separate from the Myntra vs Ajio insights
site, with no shared data, logos, or fonts.

## Setup

Node.js was not available in the environment this was written in, so this
has not been installed or run yet. On a machine with Node 18+:

```bash
npm install
npm run dev       # starts the Vite dev server
npm run build      # type-checks and builds to dist/
```

## Stack

- Vite + React 18 + TypeScript
- Tailwind CSS 3.4
- `lucide-react` for icons
- No Framer Motion — all animation is CSS `transition-*` classes

## Files

```
index.html               Fonts, root div
src/main.tsx               React entry point
src/index.css                Tailwind directives + root font stack
src/App.tsx                    The hero section (nav, mobile drawer, copy)
src/BoomerangVideoBg.tsx          Canvas frame-capture/ping-pong video loop
public/hero-loop.mp4               Background video
```

## About the background video

The original spec pointed at a CloudFront URL scoped to someone else's
account, so that couldn't be reused here. `public/hero-loop.mp4` is a
different clip — a green-plants-under-sunlight shot from
[Pexels](https://www.pexels.com) (search: "Green Plants under Sunbeams"),
used under the [Pexels License](https://www.pexels.com/license/) (free for
commercial use, no attribution required). Swap it for any other clip by
replacing that file (or pointing `BG_VIDEO` in `src/App.tsx` elsewhere) —
the boomerang effect works with any short muted video.

## Content note

The branding ("LinkFlow", "FluxEngine"), colors, copy, and nav labels are
all exactly as specified — placeholder content for this demo hero, not a
real product.

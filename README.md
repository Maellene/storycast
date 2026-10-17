# StoryCast

A 3-page accessible microsite for audio and video storytelling, built with semantic HTML5, Sass, CSS Grid, Flexbox and a container query. No frameworks.

# Project Structure
```text
storycast/
├── index.html                  Home page
├── about.html                  About / Access page
├── README.md
├── package.json
├── story/
│   ├── story.html              Story page (video, captions, transcript)
│   ├── story-2.html            Story page (audio, transcript)
│   └── story-3.html            Story page (audio, transcript)
├── css/
│   └── main.css                Compiled styles
├── sass/
│   ├── main.scss               Imports every partial
│   ├── _layers.scss            Cascade layer order
│   ├── abstracts/              Tokens: _colors, _typography, _spacing, _mixins
│   ├── base/                   _reset, _base
│   ├── layout/                 _layout (Grid layouts)
│   ├── components/             One partial per BEM block (header, nav, footer,
│   │                           button, hero, media-card, related, panel,
│   │                           transcript, story-media, skip-link)
│   └── utilities/              _utilities (visually-hidden)
├── assets/
│   ├── media/                  Images, audio and video
│   └── transcripts/            WebVTT caption file
└── docs/                       Research, sitemap and documentation PDFs
```

# Accessibility Checklist

 - Semantic HTML5 landmarks on every page: header, nav, main, article, section, aside, figure, footer
 - One h1 per page and a logical heading order (h1, h2, h3)
 - Skip link as the first focusable element on every page
 - Visible focus outline on every link, button and media control
 - Everything works with the keyboard only
 Video uses <video> with a <track kind="captions"> WebVTT file
 - Full written transcript for every audio and video story
 - <figcaption> describes each media item
 - Descriptive alt text on every image
 - aria-label on the navigation, aria-current="page" on the current link, and aria-labelledby on sections
 - Link text makes sense out of context (hidden text such as "Listen to The Snail and the Rose-Tree")
 - Text and background colors checked for WCAG AA contrast (4.5:1 for normal text)
 - Text sized in rem, readable at 200% zoom, no sideways scrolling on small screens
 - Tested with Lighthouse, axe DevTools and the W3C HTML validator

# Running Locally

You need Node.js and VS Code with the Live Server extension.

1. Clone the repository and open the folder:
bash
   git clone https://github.com/maellene/storycast.git
   cd storycast
2. Install Sass:
bash
   npm install
3. Compile Sass and watch for changes (leave this running):
bash
   npm run sass
4. In VS Code, right-click index.html and choose Open with Live Server.
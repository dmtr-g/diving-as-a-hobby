# Diving as a Hobby

A multi-page informational website about scuba diving, built with pure HTML5 and CSS3 - no JavaScript, no frameworks. Features glassmorphism UI, CSS-only carousels, animated backgrounds, and a dual-lens diving mask hero with looping video.

---

## What it does

Five interconnected pages covering why to dive, how to get certified, where the best dive locations are, and a community/contact page. The home page uses a diving mask as the hero element - two oval video lenses (playing real underwater footage) connected by a bridge, set over an animated underwater background with 27 pulsing fish icons. Built as coursework for the Web Authoring module (BSc Computing, Arden University).

---

## Demo
<img width="2442" height="1715" alt="Screenshot 2026-03-12 015650" src="https://github.com/user-attachments/assets/06f99fc6-1fa8-404a-a66a-8a81419bd50f" />
<img width="2443" height="1712" alt="Screenshot 2026-03-12 015701" src="https://github.com/user-attachments/assets/797f823c-6250-4571-9cb1-56ac60f4b578" />
<img width="2429" height="1710" alt="Screenshot 2026-03-12 015713" src="https://github.com/user-attachments/assets/fc061c04-9f71-410c-b56a-2b9dbac2f216" />
<img width="2441" height="1712" alt="Screenshot 2026-03-12 015722" src="https://github.com/user-attachments/assets/857546d8-4aaf-486b-9fcb-1d5599a756fb" />
<img width="2440" height="1706" alt="Screenshot 2026-03-12 015735" src="https://github.com/user-attachments/assets/7b727877-edfe-4d93-aa90-9ea7d37b5a3d" />

---

## Stack

| Layer | Tech |
|---|---|
| Markup | HTML5 (semantic elements, ARIA roles) |
| Styles | CSS3 - custom properties, flexbox, animations, media queries |
| Icons | Font Awesome 5.8.2 (CDN) |
| Media | MP4 video, JPEG/PNG images |
| JavaScript | None |

---

## Getting started

No build step required. Open directly in a browser:

```bash
# Clone the repo
git clone https://github.com/dmtr-g/diving-as-a-hobby.git
cd diving-as-a-hobby

# Open in browser
open index.html
```

Or drag `index.html` into any browser window. All asset paths are relative so it works from any local folder.

---

## Project structure

```
/
├── index.html                  # Home page - mask hero, animated background, search, social links
├── dmtr-g_Home.css             # Home page styles - all animations, glassmorphism, responsive
│
├── SitePages/
│   ├── dmtr-g_Why.html         # Why Diving - 5 reasons to try scuba (CSS-only carousel)
│   ├── dmtr-g_Why.css
│   ├── dmtr-g_How.html         # How to Dive - step-by-step beginner guide
│   ├── dmtr-g_How.css
│   ├── dmtr-g_Where.html       # Where to Dive - 6 best dive locations (CSS-only carousel + video)
│   ├── dmtr-g_Where.css
│   ├── dmtr-g_Who.html         # Who We Are - about section + contact form
│   └── dmtr-g_Who.css
│
└── Media/
    └── page-assets/            # Images (.jpg, .png) and videos (.mp4)
```

---

## CSS techniques used

| Technique | Where |
|---|---|
| CSS custom properties (design tokens) | All files — `--cyan`, `--glass-bg`, `--radius-pill`, etc. |
| Glassmorphism | Nav bar, mask card, glass info card — `backdrop-filter: blur()` |
| CSS-only carousel | Why and Where pages — radio inputs + sibling selectors, no JS |
| Keyframe animations | bgZoom (30s background drift), fishPulse, borderPulse, maskGlow, cardGlow |
| Dual video hero | Home — two `<video>` elements clipped to ellipses form diving mask lenses |
| Split navigation | Home — two `<nav>` blocks flanking a centred title, icons expand to show labels on hover |
| `prefers-reduced-motion` | All animations disabled for users with motion sensitivity setting |
| Responsive | 4 breakpoints: mobile (≤767px), mobile landscape, tablet (768–1023px), small desktop (1024–1200px) |

---

## What I learned / Why I built this

The brief was open-ended - build a multi-page site on any topic using only HTML and CSS. The diving mask hero was the main design challenge: getting two video elements to render as oval lenses inside a card, with a bridge element between them, required careful use of `border-radius: 50%`, `object-fit: cover`, and precise sizing with `clamp()` so the layout stayed proportional across screen sizes. Building the carousels without JavaScript - using hidden radio inputs and CSS sibling selectors - taught me how far you can push CSS before actually needing JS. The glassmorphism nav (sticky, `backdrop-filter`, expanding labels on hover without layout shift) was a separate exercise in transition handling and overflow management.


---

## Author

**Dumitru Gafincu** - [github.com/dmtr-g](https://github.com/dmtr-g) - 115009621+dmtr-g@users.noreply.github.com

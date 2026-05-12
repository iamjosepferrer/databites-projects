# databites-projects

**I'm [Josep Ferrer](https://databites.tech) — data scientist and visual educator based in Rotterdam.**  
This is where I publish my DataViz, data science, and AI projects. Real work. Shipped and public.

→ **[projects.databites.tech](https://projects.databites.tech)**

[![projects.databites.tech](https://image.thum.io/get/width/1200/crop/800/https://projects.databites.tech)](https://projects.databites.tech)

---

## What this is

A portfolio gallery that indexes every public project I build under the [DataBites](https://databites.tech) brand.

Each project gets its own subdomain (`catalonia-atlas.projects.databites.tech`) and links back to this gallery. The gallery itself is intentionally simple — one `index.html`, no framework, no build step. To add a project, I add one object to a JavaScript array and push. That's it.

---

## Live projects

### [Catalonia Income Atlas](https://catalonia-atlas.projects.databites.tech)

[![Catalonia Income Atlas](https://image.thum.io/get/width/1200/crop/800/https://catalonia-atlas.projects.databites.tech)](https://catalonia-atlas.projects.databites.tech)

An interactive choropleth map of income inequality across Catalonia — built because I wanted to understand the real shape of economic disparity in the place I'm from.

- **Data:** INE household income data, 2015–2023
- **Granularity:** 5,108 census tracts · 947 municipalities · 4 provinces
- **Stack:** MapLibre GL JS · Python (data processing) · GeoJSON

---

## Repo structure

```
databites-projects/
├── index.html              # The entire portfolio site
├── vercel.json             # Deployment config
└── images/
    ├── databitestech_logo.png
    ├── databitestech_logo_letters.png
    ├── databites_clearly_explained.png
    └── projects-headers/   # 1200×630px OG-style screenshots per project
        └── catalonia-atlas.png
```

---

## How to add a project

Open `index.html` and find the `PROJECTS` array (~line 280). Copy this object and fill in the fields:

```js
{
  id: 'your-project-id',
  title: 'Project Title',
  desc: 'One or two sentences. What it shows, what data, what tech.',
  tags: ['DataViz'],          // DataViz · Maps · ML · Tools
  chips: [
    { label: 'D3.js',   style: 'green'  },
    { label: 'Python',  style: 'forest' },
  ],
  url: 'https://your-project.projects.databites.tech/',
  screenshot: 'images/projects-headers/your-project.png',
  live: true,
  year: '2025'
},
```

Add the screenshot to `images/projects-headers/` at 1200×630px. Push to `main`. Vercel deploys automatically.

---

## Deployment

Each project is a separate Vercel deployment with its own subdomain:

| Subdomain | Repo |
|---|---|
| `projects.databites.tech` | `databites-projects` (this repo) |
| `catalonia-atlas.projects.databites.tech` | `databites-atlas` |

DNS managed via Namecheap. CNAME records point to Vercel's DNS.

---

## Brand

Everything follows the [DataBites brand guidelines](https://databites.tech):

| Token | Hex | Use |
|---|---|---|
| Forest | `#1A3829` | Text, dark backgrounds |
| Green | `#2D9B4E` | Buttons, links |
| Bright | `#38B86E` | Accents, highlights |
| Mint | `#A8DDC4` | Tints, decorative |
| Cream | `#FAF6F0` | Page canvas |

Fonts: **Lilita One** (display) · **Space Grotesk** (body) · **Space Mono** (labels, code)

---

## About me

I'm a data scientist and educator who makes complex data and AI concepts click — through diagrams, writing, and interactive tools like these. I publish weekly at [databites.tech](https://databites.tech).

→ [Newsletter](https://reads.databites.tech) · [@iamjosepferrer](https://x.com/iamjosepferrer) · [LinkedIn](https://linkedin.com/in/iamjosepferrer)
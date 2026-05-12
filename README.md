# databites-projects

**I'm [Josep Ferrer](https://databites.tech) — data scientist and visual educator based in Rotterdam.**  
This is where I publish my DataViz, data science, and AI projects. Real work. Shipped and public.

→ **[projects.databites.tech](https://projects.databites.tech)**

[![projects.databites.tech](https://api.microlink.io/?url=https://projects.databites.tech&screenshot=true&meta=false&embed=screenshot.url)](https://projects.databites.tech)

---

## What this is

A portfolio gallery that indexes every public project I build under the [DataBites](https://databites.tech) brand.

Each project gets its own subdomain (`catalonia-atlas.projects.databites.tech`) and links back to this gallery. The gallery is intentionally simple — one `index.html`, no framework, no build step. Projects are loaded from `projects.json`, the single source of truth. To add a project, I add one object to `projects.json` and push. Both this site and [databites.tech](https://databites.tech) pull from the same file automatically.

---

## Live projects

### [Catalonia Income Atlas](https://catalonia-atlas.projects.databites.tech)

[![Catalonia Income Atlas](https://api.microlink.io/?url=https://catalonia-atlas.projects.databites.tech&screenshot=true&meta=false&embed=screenshot.url)](https://catalonia-atlas.projects.databites.tech)

An interactive choropleth map of income inequality across Catalonia — built because I wanted to understand the real shape of economic disparity in the place I'm from.

- **Data:** INE household income data, 2015–2023
- **Granularity:** 5,108 census tracts · 947 municipalities · 4 provinces
- **Stack:** MapLibre GL JS · Python (data processing) · GeoJSON

---

## Repo structure

```
databites-projects/
├── index.html              # The entire portfolio site
├── projects.json           # ← single source of truth for all projects
├── vercel.json             # Deployment config
└── images/
    ├── databitestech_logo.png
    ├── databitestech_logo_letters.png
    ├── databites_clearly_explained.png
    └── projects-headers/   # 1200×630px screenshots per project
        └── catalonia-atlas.png
```

---

## How to add a project

Edit `projects.json` in the repo root. Add one object — live projects get the full format, placeholders stay compact:

```json
{
  "id": "your-project-id",
  "titleKey": "projects.yourproject.title",
  "descKey": "projects.yourproject.desc",
  "tags": ["DataViz"],
  "chips": [
    { "label": "D3.js",   "style": "green"  },
    { "label": "Python",  "style": "forest" }
  ],
  "url": "https://your-project.projects.databites.tech/",
  "screenshot": "https://projects.databites.tech/images/projects-headers/your-project.png",
  "live": true,
  "year": "2025"
}
```

Then add the matching translation strings to the `translations` object in `index.html` for EN, ES, and CA. Add the screenshot to `images/projects-headers/` at 1200×630px. Push to `main`. Vercel deploys automatically.

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
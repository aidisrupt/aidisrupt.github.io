# AI Disrupt Summit 2025 - Perth

Perth's Premier AI Builder Conference | December 13, 2025

[![Deploy](https://github.com/aidisrupt/aidisrupt.github.io/actions/workflows/static.yml/badge.svg)](https://github.com/aidisrupt/aidisrupt.github.io/actions/workflows/static.yml)

## About

The **AI Disrupt Summit** is a hands-on event shaping the future of technology in Western Australia. Taking place as part of West Tech Fest, this one-day summit brings together 200+ AI engineers, researchers, founders, and investors actively building the next generation of AI solutions.

**Presented by:** [Build Club Perth](https://www.buildclub.ai/) × [Bloom](https://www.bloom.org.au/) × [Curtin Entrepreneurs](https://www.curtin.edu.au/engage/entrepreneurs/)

**Venue:** St Catherine's College, Curtin University, Bentley WA

**Registration:** [luma.com/ywxrt4pk](https://luma.com/ywxrt4pk)

## Website Structure

```
├── index.html        # Main landing page
├── agenda.html       # Speaker Series schedule
├── expo.html         # Startup Expo profiles
├── hackathon.html    # Hackathon details
├── workshop.html     # Technical workshop info
├── demos.html        # Live demo stations
├── sundowner.html    # Networking event details
├── style.css         # Global styles
├── media/            # Images, logos, assets
├── fonts/            # Custom fonts (Ignis Sharp, HK Modular)
└── content/          # Reference materials
```

## Design System

### Perth Sunset Theme

The site uses a warm sunset color palette inspired by Perth's iconic sunsets:

| Variable            | Hex       | Usage                            |
| ------------------- | --------- | -------------------------------- |
| `--primary-color`   | `#FA8F32` | Sunset orange - CTAs, highlights |
| `--secondary-color` | `#EF6E4A` | Warm red-orange - gradients      |
| `--dark-blue`       | `#0F4A7F` | Deep blue - headings, nav        |
| `--darker-blue`     | `#0C2D4C` | Navy - hero backgrounds          |
| `--accent`          | `#FA6146` | Bright coral - accents           |
| `--sunset-orange`   | `#FAB337` | Golden orange                    |
| `--sunset-red`      | `#DE5A4A` | Sunset red                       |

### Typography

- **Headings:** Ignis Sharp (custom font)
- **Body:** System font stack (-apple-system, BlinkMacSystemFont, etc.)

## Making Changes

### Quick Text/Image Updates

1. Open the relevant HTML file
2. Find the text inside `<h1>`, `<h2>`, `<p>` tags and edit directly
3. For images: add file to `media/` folder, reference with `<img src="media/filename.png">`

### Adding a New Startup to Expo

1. Open `expo.html`
2. Find the section (AI Start-ups, Early Stage, or Idea Stage)
3. Copy an existing card block and paste within the same grid container
4. Update the details:

```html
<div class="feature-card" style="text-align: center">
  <a
    href="https://startup-website.com/"
    target="_blank"
    class="startup-logo-link"
  >
    <img src="media/startup-logo.png" alt="Startup Name logo" />
  </a>
  <h4 style="font-size: 1.4rem; margin-bottom: 5px; color: var(--dark-blue);">
    Startup Name
  </h4>
  <p style="font-size: 0.9rem; color: var(--text-light)">Founder Name</p>
</div>
```

### Adding Navigation Links

Nav is duplicated across all pages. To add a new page:

1. Create new HTML file (copy structure from existing page)
2. Add nav link to ALL pages:

```html
<a
  href="newpage.html"
  style="margin: 0 15px; font-size: 1.1rem; text-decoration: none; color: var(--dark-blue); font-weight: 700;"
  >Page Name</a
>
```

### Updating Sponsors

Sponsors appear on `index.html` (bottom) and `expo.html`. Update both when changing:

```html
<a class="sponsor-item" href="https://sponsor-url.com/" target="_blank">
  <img src="media/sponsor-logo.png" alt="Sponsor Name" class="sponsor-logo" />
  <div>
    <div class="sponsor-name">Sponsor Name</div>
    <span class="sponsor-category">Sponsor Category</span>
  </div>
</a>
```

## Local Development

```bash
# Start local server
python3 -m http.server 8080

# Open in browser
open http://localhost:8080
```

## Deployment

Site auto-deploys via GitHub Actions on push to `main` branch.

- **Workflow:** `.github/workflows/static.yml`
- **Hosting:** GitHub Pages
- **URL:** https://aidisrupt.github.io

## Key URLs

| Purpose                | URL                                                   |
| ---------------------- | ----------------------------------------------------- |
| Live Site              | https://aidisrupt.github.io                           |
| Event Registration     | https://luma.com/ywxrt4pk                             |
| Hackathon Registration | https://luma.com/3hcaaguq                             |
| Sessionize (Speakers)  | https://sessionize.com/api/v2/v08m222o/view/GridSmart |

## Sponsors

- **Bloom** - Afternoon Tea & Venue
- **Curtin Entrepreneurs** - Lunch
- **Blackbird** - Sundowner
- **Matilda Health** - Cinny Scroll
- **DDD Perth** - Community Partner
- **WADSIH** - Sponsor
- **Horst Maberly** - Sponsor
- **Lovable** - Sponsor

## Event Schedule Highlights

| Time            | Activity                                                       |
| --------------- | -------------------------------------------------------------- |
| Morning         | INSPIRE - Speaker Series (Coding Walk-throughs, Creative AI)   |
| Early Afternoon | BUILD - Hackathon, Tech Impact, AI In Practice, Workshop       |
| Mid Afternoon   | SCALE - AI Projects & Commercialisation, Scaling in Corporates |
| Late Afternoon  | CLOSE - Closing Remarks                                        |
| Evening         | Sundowner - Networking drinks (Blackbird sponsored)            |

## Contact

- **Build Club AU** ABN: 64 674 988 562
- Website: [buildclub.ai](https://www.buildclub.ai/)

---

_Part of West Tech Fest 2025_

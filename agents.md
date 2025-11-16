# AI Disrupt Summit Website - Agent Instructions

This document contains instructions for AI agents working on the AI Disrupt Summit website.

## Project Overview

This is a static single-page website for the AI Disrupt Summit 2025 conference in Perth, WA. The site is deployed via GitHub Pages and uses a sunset Perth color scheme with embedded Sessionize integration.

## Architecture

- **Single HTML file**: `index.html` with embedded CSS (no external dependencies)
- **Static assets**: Logos and images in `media/` folder
- **Deployment**: GitHub Actions workflow at `.github/workflows/static.yml`
- **Sessionize Integration**: Embedded script for speakers/sessions

## Design System

### Color Palette (Perth Sunset Theme)
```css
--primary-color: #FA8F32      /* Sunset orange */
--secondary-color: #EF6E4A    /* Warm red-orange */
--dark-blue: #0F4A7F          /* Deep blue */
--darker-blue: #0C2D4C        /* Navy blue */
--accent: #FA6146             /* Bright coral */
--sunset-orange: #FAB337      /* Golden orange */
--sunset-red: #DE5A4A         /* Sunset red */
```

### Key Design Elements
- Sunset background (`media/sunset_perth.svg`) used as subtle overlay in hero and highlight sections
- Conference logo: `media/Adobe Express - file.png` (quokka with sunglasses)
- Typography: System fonts with monospace for main title
- Responsive grid layouts for features and sponsors
- Card-based design with hover effects

## Content Structure

1. **Hero Section**
   - Logo and title
   - Event details (date, location, attendees)
   - Primary CTA (Register Now)

2. **About Section**
   - Summit description
   - Feature cards (6 items: Speaker Series, Startup Expo, Hackathon, Networking, Investor Talks, Sundowner)

3. **Speakers & Sessions**
   - Sessionize embed: `https://sessionize.com/api/v2/v08m222o/view/GridSmart`

4. **Sponsors Section**
   - Logo grid with 8 sponsors
   - Each sponsor has logo image (when available), name, and category

5. **Venue Section**
   - Location details
   - Two venue spaces described

6. **Footer**
   - Final CTA
   - Important notes

## Event Details

- **Date**: December 13, 2025 (Saturday)
- **Location**: St Catherine's College, Curtin University, Bentley WA
- **Registration**: https://luma.com/ywxrt4pk
- **Organizers**: Build Club Perth x Bloom x Curtin Entrepreneurs
- **Part of**: West Tech Fest

## Sponsors

1. Bloom (Afternoon Tea) - `media/bloom-logo.png`
2. Curtin Entrepreneurship (Lunch) - `media/curtin-logo.png`
3. Blackbird (Sundowner) - `media/blackbird-logo.svg`
4. Matilda Health (Cinny Scroll) - `media/matilda-logo.png`
5. DDD Perth (Community Partner) - `media/dddperth-logo.svg`
6. WADSIH (Sponsor) - `media/wadsih-logo.png`
7. Horst Maberly (Sponsor) - Text only
8. Lovable (Sponsor) - `media/lovable-logo.svg`

## Guidelines for Updates

### When Making Changes

1. **Maintain the sunset theme**: All color changes should use the defined color palette
2. **Keep it single-page**: Don't create additional HTML files
3. **Embedded CSS only**: All styles should remain in the `<style>` tag
4. **Responsive design**: Test on mobile and desktop
5. **Optimize images**: Use appropriate formats (SVG for logos where possible)

### Adding New Sponsors

1. Download logo in SVG or PNG format
2. Save to `media/` folder with descriptive name
3. If logo is white/light colored, edit SVG to use black fill
4. Add to sponsors grid in HTML with appropriate category
5. Maintain consistent card styling

### Content Updates

- Event details are in the hero section
- Registration link appears in hero and footer
- Sessionize script automatically updates speakers/sessions
- Location details are in the venue section

### Deployment

- Changes pushed to `main` branch automatically deploy via GitHub Actions
- No build step required (static HTML)
- GitHub Pages serves from repository root

## Common Tasks

### Update Event Date/Time
Look for date strings in hero section and update both the emoji detail boxes and any text references.

### Change Registration Link
Update the `href` in both CTA buttons (hero and footer) - search for "luma.com/ywxrt4pk"

### Modify Color Scheme
Update CSS custom properties in `:root` selector. Test contrast for accessibility.

### Add/Remove Features
Modify the `.features-grid` in the About section. Keep to 6 items for optimal grid layout.

## Technical Notes

- No JavaScript (except Sessionize embed)
- Mobile-first responsive design with `@media` queries
- CSS Grid and Flexbox for layouts
- SVG logos preferred for scalability
- All external links open in new tab (`target="_blank"`)

## Content Source Files

Reference materials are in `content/` folder:
- `linkedin.md` - Social media announcement
- `event-luma.md` - Luma event description
- `location.md` - Venue details with images

## Important Reminders

- **No emojis in code** unless explicitly requested by user
- Keep design professional and modern
- Ensure all sponsor logos are properly credited
- Maintain accessibility standards (alt text, contrast)
- Test Sessionize embed loads correctly

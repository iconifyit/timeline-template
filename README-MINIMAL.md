# Minimal Career Timeline Template

A clean, text-only career timeline built with Bootstrap 3 and a simple, classic design. Perfect for showcasing your professional journey without the distraction of images.

## Features

- **Clean, Minimal Design**: Text-only with simple color scheme
- **Bootstrap 3 Based**: Classic responsive grid system
- **JSON-Driven Content**: Easy to maintain and update
- **Three Timeline Layers**:
  - **Date Nodes** (Blue): Formal job experience with dates and achievements
  - **Narrative Nodes** (Red): Story-driven reflections and context
  - **Factoid Nodes** (Orange): Personal projects and interesting tidbits
- **Interactive Filters**: Toggle different types of content
- **Centered Timeline**: Alternating left-right layout on desktop
- **Responsive**: Stacks vertically on mobile

## Files

- `index-minimal.html` - Main HTML file
- `style-minimal.css` - Styling (based on simple-responsive-timeline)
- `timeline-data.json` - Timeline content (editable)

## Quick Start

1. Open `index-minimal.html` in your web browser
2. Edit `timeline-data.json` to customize content
3. No build process required!

## Editing Content

All timeline content is stored in `timeline-data.json`. The structure is:

```json
{
  "header": {
    "name": "Your Name",
    "subtitle": "Your Tagline",
    "links": [...]
  },
  "intro": {
    "title": "Page Title",
    "description": "Page description"
  },
  "timeline": [...]
}
```

### Timeline Item Types

**1. Narrative Node**
```json
{
  "type": "narrative",
  "info": "Label (e.g., The Mission)",
  "title": "Section Title",
  "content": "<p>HTML content here</p>"
}
```

**2. Date Node (Job)**
```json
{
  "type": "date",
  "info": "Jun 1999 – Jul 2007",
  "title": "Job Title or Company Name",
  "jobTitle": "Company | Location",
  "bullets": [
    "Achievement 1",
    "Achievement 2"
  ],
  "lesson": "Optional lesson learned"
}
```

**3. Factoid Node**
```json
{
  "type": "factoid",
  "info": "~1998-2000",
  "title": "Project Name",
  "content": "<p>Description with optional <span class=\"factoid-note\">italic note</span></p>"
}
```

**4. Period Separator**
```json
{
  "type": "period",
  "title": "2008 – 2015"
}
```

## Color Scheme

- **Text**: #768390 (gray-blue)
- **Headers**: #3D4351 (dark gray)
- **Accent**: #FF6B6B (coral/salmon)
- **Date Nodes**: #4A9EFF (blue)
- **Factoid Nodes**: #FFA94D (orange)
- **Timeline Line**: #CCD5DB (light gray)

## Customizing Colors

Edit `style-minimal.css` to change colors:

```css
/* Main accent color */
a { color: #FF6B6B; }

/* Date node color */
.timeline-item[data-type="date"] .timeline-marker:before {
  background: #4A9EFF;
}

/* Factoid node color */
.timeline-item[data-type="factoid"] .timeline-marker:before {
  background: #FFA94D;
}
```

## Adding New Timeline Items

1. Open `timeline-data.json`
2. Add a new object to the `timeline` array
3. Use one of the four types: `narrative`, `date`, `factoid`, or `period`
4. Save and refresh the page

Example:
```json
{
  "type": "date",
  "info": "Jan 2023 – Present",
  "title": "Senior Developer",
  "jobTitle": "Acme Corp | San Francisco, CA",
  "bullets": [
    "Built amazing features",
    "Led team of 5 engineers"
  ]
}
```

## Browser Compatibility

- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- IE11: ⚠️ Requires fetch polyfill

## Deployment

This is a static site that can be deployed anywhere:

- **GitHub Pages**: Push to GitHub and enable Pages
- **Netlify**: Drag and drop the folder
- **Vercel**: Import from GitHub
- **Any web server**: Upload all files to web root

## Credits

Timeline CSS based on [Simple Responsive Timeline](https://codepen.io/andrewsims/pen/WpLdMZ) by Overflow Design.

---

**Minimal. Clean. Professional.**
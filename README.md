# Animated Career Timeline Template

A beautiful, single-page, scrollable career timeline built with Tailwind CSS and smooth scroll animations. Perfect for showcasing your professional journey in an interactive and engaging way.

## Features

- **Smooth Scroll Animations**: Timeline items fade in as you scroll down the page
- **Dual Timeline Structure**:
  - **Date Nodes**: Cyan-colored cards with dates and job details from your resume
  - **Narrative Nodes**: Story-driven cards that weave context and personality between jobs
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Modern UI**: Built with Tailwind CSS for a clean, professional look
- **Alternating Layout**: Timeline events alternate between left and right for visual interest
- **Placeholder Images**: Uses Unsplash images that you can easily replace with your own
- **Gradient Accents**: Eye-catching gradient colors for headers and highlights
- **Interactive Cards**: Hover effects on timeline cards for better engagement
- **Visual Hierarchy**: Distinct styling for date nodes (cyan border + gradient badge) vs narrative nodes (purple/pink accents)

## Quick Start

1. Simply open `index.html` in your web browser
2. No build process or dependencies required!

## Customization Guide

### Replacing Placeholder Images

Find all image tags in the HTML:

```html
<img src="https://images.unsplash.com/photo-xxxxx?w=800&h=400&fit=crop"
     alt="Section Title"
     class="w-full h-48 object-cover rounded-lg">
```

Replace with your own images:
- **Option 1**: Use your own hosted images (upload to your server)
- **Option 2**: Use a relative path to local images:
  ```html
  <img src="./images/my-photo.jpg" alt="Section Title" class="...">
  ```
- **Option 3**: Keep using Unsplash but search for better matches at [unsplash.com](https://unsplash.com)

### Understanding the Two Types of Nodes

The timeline uses two distinct types of nodes:

**1. Date Nodes (Job Experience)**
- Cyan/teal colored with gradient date badges
- Larger timeline dots with a cyan border and glow effect
- Contains: dates, company, location, job title, and bullet points
- Uses the `date-node` class for the cyan left border
- Uses the `timeline-dot-date` class for the larger timeline dot

**2. Narrative Nodes (Story Elements)**
- Purple, pink, orange, or other accent colors
- Standard blue timeline dots
- Contains: stories, reflections, and context that connect the jobs
- Uses standard `timeline-dot` class

### Modifying Content

**Date Node Structure:**
```html
<div class="timeline-item mb-32 relative">
    <div class="timeline-dot-date hidden md:block"></div>
    <div class="md:w-1/2 md:ml-auto md:pl-12">
        <div class="bg-white rounded-lg p-8 card-shadow date-node">
            <div class="date-badge text-white px-4 py-2 rounded-lg inline-block mb-4">
                <div class="text-sm font-semibold">Jun 1999 – Jul 2007</div>
            </div>
            <!-- Image, job title, company, bullet points -->
        </div>
    </div>
</div>
```

**Narrative Node Structure:**
```html
<div class="timeline-item mb-32 relative">
    <div class="timeline-dot hidden md:block"></div>
    <div class="md:w-1/2 md:pr-12">
        <div class="bg-white rounded-lg p-8 card-shadow">
            <!-- Image, badge, story content -->
        </div>
    </div>
</div>
```

- **Left-aligned items**: Use `md:pr-12` (no `md:ml-auto`)
- **Right-aligned items**: Use `md:ml-auto md:pl-12`

### Adding New Timeline Events

Copy an existing timeline event and modify:

1. Copy the entire `timeline-item` div
2. Paste it where you want it in the timeline
3. Update the content, image, and badge color
4. Alternate between left and right alignment for visual balance

### Changing Colors

The template uses these color schemes:
- **Badges**: `bg-blue-100 text-blue-800`, `bg-purple-100 text-purple-800`, etc.
- **Gradients**: Modify in the gradient-text class and timeline-line
- **Timeline dots**: Default blue border, final one is pink

To change badge colors, replace the class:
```html
<span class="inline-block bg-green-100 text-green-800 text-sm font-semibold px-3 py-1 rounded-full mb-4">
    Your Label
</span>
```

Available Tailwind colors: blue, purple, green, orange, red, pink, indigo, yellow, etc.

### Adjusting Animation Speed

In the `<style>` section, modify the transition duration:

```css
.timeline-item {
    transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}
```

Change `0.8s` to your preferred duration (e.g., `1.2s` for slower, `0.5s` for faster).

### Modifying the Gradient

Update the gradient in the `<style>` section:

```css
.timeline-line {
    background: linear-gradient(to bottom, #3b82f6, #8b5cf6, #ec4899);
}
```

Or for the header text:

```css
.gradient-text {
    background: linear-gradient(135deg, #3b82f6, #8b5cf6);
}
```

## Project Structure

```
timeline-template/
├── index.html          # Main timeline page
└── README.md          # This file
```

## Browser Compatibility

- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Mobile browsers: ✅ Full support

## Technologies Used

- **Tailwind CSS**: Utility-first CSS framework (loaded via CDN)
- **Intersection Observer API**: For scroll-based animations
- **Google Fonts**: Inter font family for clean typography
- **Unsplash**: Placeholder images

## Tips for Best Results

1. **Images**: Use high-quality images with a 2:1 aspect ratio (800x400px recommended)
2. **Content Length**: Keep each timeline event concise (2-3 paragraphs max)
3. **Testing**: Test on multiple devices and screen sizes
4. **Performance**: If using custom images, optimize them first (use tools like TinyPNG)
5. **Personalization**: Replace ALL placeholder content with your actual career information

## Next Steps

1. Replace all placeholder images with your own photos
2. Update the hero section with your actual contact links
3. Customize colors to match your personal brand
4. Add or remove timeline events as needed
5. Test on mobile devices
6. Deploy to your hosting service (GitHub Pages, Netlify, Vercel, etc.)

## Deployment Options

### GitHub Pages
1. Push this repo to GitHub
2. Go to Settings > Pages
3. Select the main branch
4. Your site will be live at `https://yourusername.github.io/timeline-template`

### Netlify
1. Drag and drop the folder to [Netlify Drop](https://app.netlify.com/drop)
2. Your site will be live instantly

### Vercel
1. Push to GitHub
2. Import the repo in [Vercel](https://vercel.com)
3. Deploy with one click

## License

Feel free to use this template for your personal portfolio or job applications!

---

**Built with ❤️ for showcasing amazing careers**

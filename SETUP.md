# Jekyll GitHub Pages Site - Setup Guide

This is a personal website built with Jekyll and hosted on GitHub Pages, featuring a retro early-2000s aesthetic.

## Features

- **Retro Aesthetic**: Monospaced Courier New font, classic blue/purple hyperlinks, minimal CSS
- **Jekyll-Powered**: Static site generator with Markdown support
- **GitHub Pages Compatible**: Uses the official `github-pages` gem
- **Embedded Content Support**: Ready for LinkedIn, Google Scholar, GitHub widgets, and more

## File Structure

```
.
├── _config.yml          # Jekyll configuration
├── _layouts/            # Page layouts
│   └── default.html     # Main layout template
├── assets/
│   └── css/
│       └── style.css    # Retro-styled CSS
├── index.md             # Homepage
├── about.md             # About page
├── projects.md          # Projects page
├── contact.md           # Contact page
├── Gemfile              # Ruby dependencies
└── .gitignore           # Git ignore rules
```

## Quick Start

### Local Development

1. **Install Ruby and Bundler** (if not already installed):
   ```bash
   gem install bundler
   ```

2. **Install dependencies**:
   ```bash
   bundle install
   ```

3. **Build the site**:
   ```bash
   bundle exec jekyll build
   ```

4. **Serve locally**:
   ```bash
   bundle exec jekyll serve
   ```
   
   Visit `http://localhost:4000` in your browser.

### GitHub Pages Deployment

1. Push your changes to the `main` or `gh-pages` branch
2. Enable GitHub Pages in your repository settings
3. Your site will be available at `https://yourusername.github.io`

## Customization

### Update Site Information

Edit `_config.yml`:
```yaml
title: Your Name
description: Your site description
url: "https://yourusername.github.io"
```

### Customize Content

- **Homepage**: Edit `index.md`
- **About**: Edit `about.md`
- **Projects**: Edit `projects.md`
- **Contact**: Edit `contact.md`

### Add Embedded Content

#### LinkedIn Profile Badge

In `about.md`, replace the placeholder with:
```html
<div class="embed-container">
<script src="https://platform.linkedin.com/badges/js/profile.js" async defer type="text/javascript"></script>
<div class="badge-base LI-profile-badge" data-locale="en_US" data-size="medium" data-theme="light" data-type="VERTICAL" data-vanity="your-profile" data-version="v1">
  <a class="badge-base__link LI-simple-link" href="https://www.linkedin.com/in/your-profile?trk=profile-badge">Your Name</a>
</div>
</div>
```

#### Google Scholar Link

Update the Google Scholar URL in `about.md`:
```html
<a href="https://scholar.google.com/citations?user=YOUR_USER_ID" target="_blank">Google Scholar</a>
```

#### GitHub Activity Chart

Already included in `projects.md`:
```html
<img src="https://ghchart.rshah.org/yourusername" alt="GitHub Contributions" />
```

#### Contact Form (Google Forms)

In `contact.md`, add your Google Form embed:
```html
<iframe src="https://docs.google.com/forms/d/e/YOUR_FORM_ID/viewform?embedded=true" width="640" height="500" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
```

### Modify Styling

Edit `assets/css/style.css` to customize:
- Fonts (currently Courier New)
- Colors (link colors, backgrounds)
- Layout and spacing
- Border styles

### Add New Pages

1. Create a new `.md` file (e.g., `blog.md`)
2. Add front matter:
   ```yaml
   ---
   layout: default
   title: Blog
   ---
   ```
3. Add your Markdown content
4. Update navigation in `_layouts/default.html`

## Tips

- **Markdown**: All content pages use Markdown for easy formatting
- **Raw HTML**: You can mix HTML directly in Markdown files for embeds
- **Jekyll Liquid**: Use `{{ }}` and `{% %}` for dynamic content
- **Front Matter**: Every page needs YAML front matter with `layout` and `title`

## Troubleshooting

### Build Errors

- Make sure all dependencies are installed: `bundle install`
- Check Ruby version: `ruby --version` (should be 2.7+)
- Clear cache: `bundle exec jekyll clean`

### Broken Links

- Use relative URLs: `{{ '/about/' | relative_url }}`
- Jekyll uses "pretty" permalinks by default (no `.html` extension)

### Styling Issues

- Clear browser cache
- Check that CSS file path is correct in layout
- Rebuild site: `bundle exec jekyll build`

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [Liquid Template Language](https://shopify.github.io/liquid/)

## License

This template is free to use and modify for your personal website.

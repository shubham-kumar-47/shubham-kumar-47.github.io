# Shubham Kumar | AI/ML Engineer Portfolio

Personal portfolio website built with Jekyll, featuring a dark SaaS-style design with glassmorphism cards, gradient accents, and scroll-reveal animations.

**Live:** [shubham-kumar-47.github.io](https://shubham-kumar-47.github.io)

## About Me

Snowflake Certified Data Science / AI/ML / Generative & Agentic AI / Data Engineering Professional with 7+ years of experience. Specializing in building intelligent systems across Banking & Finance, Retail, Fraud & Securities, and SaaS domains.

Currently working as an **AI/ML Engineer at Blue.Cloud**, designing multi-agent systems (SnowMigrate360, SnowML360) and leading enterprise data architecture initiatives on Snowflake.

## Tech Stack

- **Framework:** Jekyll (static site generator)
- **Styling:** Custom SCSS with dark theme, glassmorphism, gradient animations
- **Content:** YAML-driven (single `_data/portfolio.yml` file)
- **Deployment:** GitHub Pages via GitHub Actions
- **Dev Environment:** VS Code DevContainer (Ruby 3.2)

## Project Structure

```
.
├── .devcontainer/          # DevContainer config (Ruby + Jekyll)
├── .github/workflows/      # GitHub Actions for auto-deployment
├── _data/
│   └── portfolio.yml       # All site content (edit this to update)
├── _includes/
│   ├── nav.html            # Navigation bar
│   ├── footer.html         # Footer
│   └── sections/           # Page sections (hero, about, career, etc.)
├── _layouts/
│   ├── default.html        # Main layout
│   └── post.html           # Blog post layout
├── _sass/
│   ├── _variables.scss     # Theme colors, fonts, spacing
│   ├── _base.scss          # Reset, typography, buttons
│   ├── _components.scss    # Cards, timeline, skill bars
│   ├── _sections.scss      # Section-specific styles
│   ├── _animations.scss    # Scroll reveal, keyframes
│   └── _responsive.scss    # Mobile breakpoints
├── assets/
│   ├── css/main.scss       # SCSS entry point
│   └── images/             # Site images (avatar, project logos)
├── _config.yml             # Jekyll configuration
├── Gemfile                 # Ruby dependencies
├── index.html              # Single-page layout
└── Shubham_K_CV_2026_May.pdf  # Downloadable CV
```

## Sections

| Section | Description |
|---------|-------------|
| **Hero** | Full-viewport intro with avatar, name, tagline, CTAs |
| **About** | Profile summary, highlights, experience stats |
| **Career** | Vertical timeline of professional experience |
| **Skills** | Categorized skill bars (AI/ML, Programming, Cloud, DevOps) + Certifications |
| **Projects** | Grid of project cards with tags and descriptions |
| **Contact** | Email, phone, social links, CV download, education |

## Local Development

### Using DevContainer (Recommended)

1. Open in VS Code
2. Reopen in Container (Ctrl+Shift+P > "Dev Containers: Reopen in Container")
3. Site auto-serves at `http://localhost:4000`

### Manual Setup

```bash
# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Open http://localhost:4000
```

## Updating Content

All content is driven by `_data/portfolio.yml`. Edit this file to:

- Update profile info, career history, skills
- Add new projects or certifications
- Change contact details or social links
- Add/reference images (place in `assets/images/`)

## Deployment

Automatic via GitHub Actions on push to `main`. The workflow:
1. Builds the Jekyll site
2. Deploys to GitHub Pages

No manual deployment steps needed.

## Adding Images

1. Place image files in `assets/images/`
2. Reference them in `_data/portfolio.yml`:
   ```yaml
   image: "/assets/images/your-image.png"
   ```

## License

MIT

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Essential Commands

### Development
```bash
# Install dependencies (required first time)
bundle install
npm install

# Run local development server with live reload
bundle exec jekyll serve --livereload
# Visit http://localhost:4000

# Alternative: Docker development (if Ruby issues)
docker-compose up
```

### Testing & Validation
```bash
# Run all linters
npm run lint

# Fix auto-fixable lint issues  
npm run lint:fix

# Run individual linters
npm run lint:md    # Markdown
npm run lint:css   # CSS
npm run lint:js    # JavaScript

# Full test suite (lint + build)
npm run test

# Build production site
npm run build
```

### Git Workflow
```bash
# The site auto-deploys to GitHub Pages when pushing to main branch
git add .
git commit -m "Add new [feature/content]"
git push origin main
```

## Architecture Overview

### Jekyll Static Site Structure
This is a Jekyll-based family website hosted on GitHub Pages. The site uses Jekyll collections for different content types and follows a component-based layout system.

### Content Organization
- **_posts/**: Blog posts in format `YYYY-MM-DD-title.md` - family updates and articles
- **_projects/**: Project showcases with metadata for technologies and collaborators  
- **_family_moments/**: Family memories and photos with family member tags
- **_layouts/**: Reusable page templates (default, post, project, moment)
- **assets/**: Static resources (CSS, JavaScript, images)

### Key Configuration
- **_config.yml**: Site settings, family member profiles, Jekyll plugins, and collection definitions
- **Gemfile**: Ruby dependencies including Jekyll and GitHub Pages gems
- **package.json**: Node.js tooling for linting and development workflow

### Templating System
The site uses Liquid templating with a hierarchical layout structure:
- `default.html`: Base template with header, footer, and navigation
- Content-specific layouts inherit from default and add specialized rendering

### Family Member System
Family members are defined in `_config.yml` with emoji, color, and description attributes. These are used throughout the site for authorship attribution and theming.

### Deployment Pipeline
GitHub Actions CI/CD workflow (`.github/workflows/ci.yml`):
1. **Lint**: Validates markdown, HTML, and checks for issues
2. **Build**: Compiles Jekyll site with production settings
3. **Test**: Validates generated HTML and checks performance
4. **Deploy**: Automatically publishes to GitHub Pages on main branch pushes

### Local Development Options
Multiple approaches documented in `LOCAL_DEVELOPMENT.md`:
- Native Ruby installation (Ruby 3.0+ required)
- Docker containers for consistent environment
- Direct GitHub editing for simple changes

## Development Notes

### Adding Content
- Posts, projects, and moments follow Jekyll front matter conventions
- Each content type has specific metadata requirements (see README.md examples)
- Images should be optimized and placed in `assets/images/`

### Styling
- Uses custom CSS with Fredoka font family for playful aesthetic
- Frog-themed color scheme defined in family member profiles
- Responsive design with mobile-first approach

### JavaScript
- Minimal JavaScript for navigation toggle and interactive elements
- Located in `assets/js/main.js`

### Performance Considerations
- CI/CD checks for large files (>1MB) and images (>500KB)
- Jekyll build optimization through pagination and selective regeneration
- GitHub Pages CDN handles production serving
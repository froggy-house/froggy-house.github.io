# The Froggy House 🐸

Welcome to our family website repository! This is where the Froggy Family shares projects, memories, and adventures.

## 🌟 Quick Start

### View the Website

Visit our live site at: [https://froggy-house.github.io](https://froggy-house.github.io)

### Local Development

1. **Clone the repository**

   ```bash
   git clone https://github.com/froggy-house/froggy-house.github.io.git
   cd froggy-house.github.io
   ```

2. **Install dependencies**

   ```bash
   bundle install
   npm install
   ```

3. **Run locally**

   ```bash
   bundle exec jekyll serve
   ```

   Visit `http://localhost:4000` in your browser

## 📝 Adding Content

### Creating a Blog Post

Create a new file in `_posts/` with the format `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: "Your Post Title"
date: 2024-01-15
categories: [Project]
tags: [coding, fun]
author: "Smart Frog"
author_emoji: "🎓"
---

Your content here...
```

### Adding a Project

Create a file in `_projects/`:

```markdown
---
layout: project
title: "Project Name"
date: 2024-01-15
featured_image: /assets/images/project.jpg
technologies: [JavaScript, HTML, CSS]
collaborators: ["Daddy Frog", "Smart Frog"]
---

Project description...
```

### Sharing Family Moments

Create a file in `_family_moments/`:

```markdown
---
layout: moment
title: "Memory Title"
date: 2024-01-15
photo: /assets/images/moment.jpg
family_members: ["Smart Frog", "Baby Robot Frog"]
---

Memory description...
```

## 🛠️ Development

### Linting

```bash
# Run all linters
npm run lint

# Fix auto-fixable issues
npm run lint:fix
```

### Testing

```bash
npm run test
```

## 🚀 Deployment

The site automatically deploys to GitHub Pages when you push to the `main` branch. The CI/CD pipeline will:

1. Run linters on your code
2. Build the Jekyll site
3. Validate HTML and check for issues
4. Deploy to GitHub Pages

## 📁 Project Structure

```text
froggy-house.github.io/
├── _posts/          # Blog posts
├── _projects/       # Project showcases
├── _family_moments/ # Family memories
├── _layouts/        # Page templates
├── assets/
│   ├── css/        # Stylesheets
│   ├── js/         # JavaScript
│   └── images/     # Images
├── _config.yml     # Jekyll configuration
├── Gemfile         # Ruby dependencies
└── package.json    # Node dependencies
```

## 👨‍👩‍👧‍👦 The Froggy Family

- 🐸 **Daddy Frog** - The wise coder
- 🌸 **Mommy Frog** - The creative organizer
- 🎓 **Smart Frog** - The curious learner
- 🤖 **Baby Robot Frog** - The tech-savvy little one

## 📄 License

This project is maintained by the Froggy Family with love 💚

## 🤝 Contributing

This is our family website, but we love seeing how others use our projects! Feel free to:

- Fork the repository for your own family site
- Open issues if you find bugs
- Share your creations inspired by our work

---

Made with 💚 by the Froggy Family

+++
title = 'Setting Up a Technical Blog with Hugo'
date = '2025-01-09'
draft = false
+++

Today I set up this blog using Hugo, a fast and flexible static site generator. Here's a walkthrough of the process for anyone interested in creating their own technical blog.

## AI Collaboration

This blog setup was completed with the assistance of Claude, an AI assistant by Anthropic. Using AI tools effectively is an important part of modern development workflow. Claude helped with:

- Troubleshooting Hugo installation and configuration
- Crafting site content and structure
- Git repository setup
- GitHub Pages deployment steps

While Claude provided guidance, all implementation decisions and code verification were done by me. This project demonstrates how AI can be used as an effective tool for technical tasks while maintaining human oversight and decision-making.

## Initial Setup

1. Installed Hugo Extended using Chocolatey:

```bash
choco install hugo-extended -y
```

2. Created a new site:

```bash
hugo new site myblog
cd myblog
git init
```

3. Added the Ananke theme:

```bash
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
```

## Configuration

The site configuration in hugo.toml includes:

```toml
baseURL = 'https://jamieroszel22.github.io/my_blog/'
languageCode = 'en-us'
title = 'Project Workbench'
theme = 'ananke'
publishDir = 'docs'

[params]
  description = "A technical log tracking software projects, dev experiments, and engineering insights."
  background_color_class = "bg-black"
  featured_image = "/images/project_workbench_hero.jpeg"
  site_logo = "/images/project_workbench_logo.jpg"
  ```

## GitHub Pages Deployment

1. Created a GitHub repository
2. Added remote origin and pushed code
3. Configured GitHub Pages to deploy from /docs folder in the master branch
4. Updated hugo.toml with correct baseURL and publishDir

## Structure

The site maintains a simple structure:

- /content/posts/ - Blog posts
- /content/about/ - About page
- /static/images/ - Site images and assets
- /docs/ - Generated site for GitHub Pages

## Going Forward

This blog will serve as a technical journal for documenting projects, experiments, and learnings in software development. Next steps include:

- Adding more detailed technical posts
- Customizing the theme
- Setting up categories and tags
- Implementing a commenting system

Stay tuned for more technical content!

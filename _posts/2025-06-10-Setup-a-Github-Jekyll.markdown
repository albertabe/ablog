---
layout: post
title: "How to Set Up GitHub Pages with Jekyll"
date: 2025-06-10
categories: [jekyll, github]
tags: [webdev, blogging, static-site]
author: abe
---

# How to Set Up GitHub Pages with Jekyll

Jekyll is a static site generator that integrates seamlessly with **GitHub Pages**, allowing you to host a blog or website for free. Here's a step-by-step guide to get started.

---

## **Prerequisites**
1. A **GitHub account** ([sign up here](https://github.com/)).
2. **Ruby** (v2.5.0 or higher) and **RubyGems** installed.
3. **Bundler** (for dependency management).
4. **Git** (for version control).

---

## **Step 1: Install Jekyll**
Open a terminal and run:

```bash
gem install jekyll bundler

Verify the installation:
bash

jekyll -v
# Output should show the version (e.g., `jekyll 4.3.3`)

##**Step 2: Create a New Jekyll Site**

Generate a new site:
bash

jekyll new my-blog
cd my-blog

This creates a basic Jekyll structure:
text

my-blog/
├── _posts/       # Blog posts go here
├── _config.yml   # Site configuration
├── Gemfile       # Dependencies
└── index.md      # Homepage

## **Step 3: Run the Site Locally**

Start a local server:
bash

bundle exec jekyll serve

Visit http://localhost:4000 to preview your site.
##**Step 4: Set Up GitHub Pages**

    Create a new GitHub repo named <username>.github.io (replace <username> with your GitHub handle).

    Push your Jekyll site to GitHub:

bash

git init
git add .
git commit -m "Initial Jekyll setup"
git remote add origin https://github.com/<username>/<username>.github.io.git
git push -u origin main

GitHub Pages will automatically deploy your site to:
text

https://<username>.github.io

##**Step 5: Customize Your Site**
Edit _config.yml
yaml

title: My Awesome Blog
description: A blog about tech and life
url: "https://<username>.github.io"
theme: minima  # Default theme (change if needed)

Add a New Post

    Create a file in /_posts/ with the format YYYY-MM-DD-title.md.

    Include front matter:

markdown

---
title: "My First Post"
date: 2024-05-21
---

##**Step 6: Use a Custom Theme (Optional)**

Browse Jekyll themes and update _config.yml:
yaml

theme: "theme-name"

Or install manually via Gemfile:
ruby

gem "theme-name"

Run bundle install and restart Jekyll.
Troubleshooting

    Broken links? Run bundle exec jekyll build --trace for debugging.

    GitHub Pages not updating? Wait ~2 minutes or check the Actions tab in your repo.
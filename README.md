# DevOps Demo - Code-to-Live-in-60-Seconds

A simple demo project for training freshers on DevOps concepts using GitHub Actions and GitHub Pages.

## Purpose

This project is designed for the "Code-to-Live-in-60-Seconds" DevOps training demo. It demonstrates how code changes can be automatically deployed to a live website without manual server intervention.

## Setup Instructions (15-min prep before class)

### 1. Create GitHub Repository
- Create a new GitHub repository (public or private)
- Initialize it with this code
- The repository name should be in the format: `yourusername.github.io` (for GitHub Pages) or any name you prefer

### 2. Enable GitHub Pages
- Go to repository **Settings** → **Pages**
- Under **Build and deployment**, set **Source** to **GitHub Actions**
- This tells GitHub to use the workflow file in `.github/workflows/deploy.yml`

### 3. Enable GitHub Actions
- Go to repository **Settings** → **Actions** → **General**
- Under **Actions permissions**, select **Allow all actions and reusable workflows**
- Click **Save**

### 4. Initial Deployment
- Push the code to the `main` branch
- Go to the **Actions** tab to watch the workflow run
- Once it completes (green checkmark), your site will be live at: `https://yourusername.github.io/repository-name/`

### 5. Prepare for Demo
Open these three browser tabs before the demo:
- **Tab 1**: The live website (your GitHub Pages URL)
- **Tab 2**: The GitHub repository's **Actions** tab
- **Tab 3**: Your code editor (VS Code) with `index.html` open

## Demo Script

### Act 1 - The Pain (3 min)
Tell the story about the old way of deploying websites - zipping files, emailing to server guy, manual uploads, things breaking, blame games.

### Act 2 - The Magic (10 min)
1. Show the live website (Tab 1)
2. Change the heading in `index.html` (Tab 3):
   ```html
   <!-- Change from -->
   <h1>Welcome to BinaryBrains</h1>
   <!-- To -->
   <h1>DevOps is Awesome 🚀</h1>
   ```
3. Push the changes:
   ```bash
   git add .
   git commit -m "Update heading"
   git push
   ```
4. Show the GitHub Actions tab (Tab 2) - watch the yellow spinner turn green
5. Refresh the live website (Tab 1) - the change is now live!

### Act 3 - Break It On Purpose (5 min)
1. Introduce a deliberate mistake (e.g., break the HTML)
2. Push the broken code
3. Show the pipeline go RED in Actions tab
4. Fix and re-push - watch it turn GREEN again
5. Explain how DevOps protects against shipping bugs

### Debrief (5 min)
Now introduce the terminology:
- **Version Control (Git)** - Saving versions with `git`
- **CI** - Continuous Integration (robot grabbing & checking code)
- **CD** - Continuous Deployment (robot putting it live)
- **Pipeline** - The whole automatic flow
- **Automated Testing** - Robot blocking broken code
- **Automation** - Nobody touching a server by hand

## File Structure

```
devops-demo/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions workflow for auto-deployment
├── index.html                  # Simple webpage with editable heading
├── README.md                   # This file
└── .gitignore                  # Git ignore rules
```

## Key Points for Trainers

1. **Show before you name** - No jargon until the debrief table
2. **Protect the "wow"** - Pause after the live site refreshes
3. **Always have a backup** - Record the demo in case internet fails
4. **Keep it simple** - One heading change is enough to demonstrate the concept

## Common Questions

**Q: Who is the robot?**
A: GitHub Actions. There are many similar tools: Jenkins, GitLab CI, CircleCI, etc.

**Q: Do I need to know coding for this?**
A: You'll learn the bits you need. DevOps is more about automating than writing apps from scratch.

**Q: Is this hard?**
A: You just understood a real CI/CD pipeline in 20 minutes. You're already started!

## One-Line Summary

> **DevOps = type 3 lines, and a robot safely puts your work in front of the world.**

## Backup Plan

Always have a recorded screen capture of the full demo as backup. If Wi-Fi dies during the live demo, play the recording and narrate exactly the same way.

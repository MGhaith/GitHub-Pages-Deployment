# GitHub Pages Deployment

A streamlined GitHub Actions workflow for deploying static websites to GitHub Pages with minimal configuration.

## Overview

This project provides an automated deployment pipeline that simplifies the process of publishing static websites to GitHub Pages. It's designed to work seamlessly with Hugo static sites but can be adapted for other static site generators.

## Features

- **Zero-Config Deployment**: Automatically deploys your static site to GitHub Pages with minimal setup
- **GitHub Actions Integration**: Leverages GitHub's CI/CD infrastructure for reliable deployments
- **Secure Authentication**: Uses GitHub's built-in authentication for secure deployments
- **Customizable Workflow**: Easily adaptable for different static site generators
- **Automatic Builds**: Triggers deployments on push to main branch or manually via workflow dispatch

## How It Works

The workflow:
1. Checks out your repository
2. Sets up GitHub Pages environment
3. Uploads your static site as an artifact
4. Deploys the artifact to GitHub Pages

## Getting Started

### Prerequisites

- A GitHub account
- A repository with a static website using [Hugo](/https://gohugo.io/), [Jekyll](https://jekyllrb.com/), or plain HTML
- Repository permissions to enable [GitHub Pages](https://docs.github.com/en/pages)

### Setup

1. **Fork or clone this repository**

2. **Configure your static site**
   - Place your static site files in the `gh-deployment-workflow` directory
   - Update the configuration in `gh-deployment-workflow/hugo.toml` (for Hugo sites)

3. **Enable GitHub Pages**
   - Go to your repository settings
   - Navigate to Pages
   - Select "GitHub Actions" as the source

4. **Push to main branch**
   - The workflow will automatically deploy your site

### Manual Deployment

You can manually trigger the deployment from the Actions tab in your GitHub repository.

## Customization

### For Different Static Site Generators

Modify the `.github/workflows/deploy.yml` file to accommodate your specific static site generator's build process.

### Custom Domain

To use a custom domain:
1. Update the `baseURL` in your site configuration
2. Add a CNAME file to your static directory

## Technical Details

The deployment uses GitHub's official Actions:
- `actions/checkout@v4`
- `actions/configure-pages@v4`
- `actions/upload-pages-artifact@v4`
- `actions/deploy-pages@v4`

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/MGhaith/GitHub-Pages-Deployment/blob/main/LICENSE) file for details.
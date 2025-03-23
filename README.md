# WordPress Content Manager

A system for managing WordPress content using GitHub for versioning and OSP (Open Strategy Partners) tools for content optimization.

## Features

- Sync WordPress posts and pages with GitHub
- Use GitHub for content versioning and collaboration
- Apply OSP writing standards for content quality
- Optimize content for SEO
- Manage images from Envato or other sources
- Automate deployment back to WordPress

## Setup

### Requirements

- WordPress site(s) with admin access
- GitHub repository
- GitHub Personal Access Token with appropriate permissions
- WordPress GitHub Sync plugin installed on your WordPress site

### Configuration

1. Install the WordPress GitHub Sync plugin on your WordPress site
2. Configure the plugin with your GitHub credentials
3. Set up GitHub Actions workflows for automation
4. Configure OSP tools for content optimization

## Usage

### Content Workflow

1. Create or edit content in WordPress
2. Content is automatically synced to GitHub
3. Make additional edits via GitHub if needed
4. Run OSP optimization workflows
5. PR review process for content quality
6. Deploy approved content back to WordPress

### Image Management

1. Search for images in Envato or other sources
2. Download and optimize images
3. Add images to the GitHub repository
4. Reference images in your content
5. Images are deployed to WordPress with content

## Folder Structure

- `/posts/` - WordPress posts
- `/pages/` - WordPress pages
- `/images/` - Image assets
- `/seo-config/` - SEO configuration and metadata
- `/.github/workflows/` - GitHub Actions workflow definitions
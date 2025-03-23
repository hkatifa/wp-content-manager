# Installation Guide

This guide will help you set up the WordPress-GitHub integration system for content management.

## Prerequisites

Before you begin, make sure you have the following:

1. WordPress site with admin access
2. GitHub account
3. Basic knowledge of WordPress, GitHub, and content management

## Step 1: Set Up GitHub Repository

You've already completed this step if you're reading this guide. The repository contains the basic structure for managing WordPress content via GitHub.

## Step 2: Install WordPress GitHub Sync Plugin

1. Download the WordPress GitHub Sync plugin from [GitHub](https://github.com/mAAdhaTTah/wordpress-github-sync)
2. Install and activate the plugin on your WordPress site:
   - Go to WordPress Admin > Plugins > Add New > Upload Plugin
   - Upload the ZIP file and activate the plugin

## Step 3: Configure WordPress GitHub Sync

1. Navigate to Settings > GitHub Sync in your WordPress admin
2. Configure the following settings:
   - GitHub Repository: `hkatifa/wp-content-manager` (or your own repository)
   - GitHub Branch: `main`
   - GitHub OAuth Token: Create a personal access token in GitHub with the `repo` scope
   - Webhook Secret: Create a random string to secure the webhook communication

3. Configure export settings:
   - Default Export Branch: `main`
   - Post Types to Export: Select which post types to sync (typically `post` and `page`)

## Step 4: Set Up GitHub Webhook

1. Go to your GitHub repository > Settings > Webhooks > Add webhook
2. Configure the webhook:
   - Payload URL: `https://your-wordpress-site.com/wp-json/wpghs/v1/webhook`
   - Content Type: `application/json`
   - Secret: Use the same secret from Step 3
   - Events: Select "Just the push event"

## Step 5: Initial Content Export

1. In WordPress admin, go to Tools > Export to GitHub
2. Click "Export to GitHub" to perform the initial export of your content

## Step 6: Configure OSP Integration

1. Install the OSP tools for content optimization:
   ```bash
   npm install osp-tools
   ```

2. Configure OSP settings in `config/osp-config.json`

## Step 7: Configure Envato Image Integration

1. Get your Envato API key from your Envato account
2. Add the API key to `config/wp-sync-config.json` in the `image_sources` section

## Step 8: Test the Integration

1. Create a new post in WordPress
2. Check GitHub to verify the post was synced
3. Make changes in GitHub and push them
4. Verify the changes appear in WordPress

## Troubleshooting

### Content Not Syncing from WordPress to GitHub

1. Check the WordPress GitHub Sync settings
2. Verify your GitHub OAuth token has the correct permissions
3. Check for errors in the WordPress GitHub Sync logs

### Content Not Syncing from GitHub to WordPress

1. Verify the webhook is configured correctly
2. Check that the webhook secret matches
3. Ensure the correct branch is being monitored

### Image Import Issues

1. Check your Envato API key
2. Verify the image paths in your content
3. Ensure the images directory is writable

## Next Steps

After installation, you can:

1. Customize the SEO guidelines in `seo-config/seo-guidelines.json`
2. Set up GitHub Actions for automated content optimization
3. Add more WordPress sites to the configuration

For more information, see the [README.md](README.md) file.

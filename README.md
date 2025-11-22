# Start Page

Beautiful background images that auto-change every 30 minutes. Perfect Safari start page.

## Setup with GitHub Secrets

### 1. Get Unsplash API Key

1. Go to [Unsplash Developers](https://unsplash.com/developers)
2. Sign up for a free developer account
3. Create a new application
4. Copy your Access Key

### 2. Add GitHub Secret

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Navigate to "Secrets and variables" > "Actions"
4. Click "New repository secret"
5. Add secret with name: `UNSPLASH_ACCESS_KEY`
6. Paste your Unsplash Access Key as the value
7. Click "Add secret"

### 3. Enable GitHub Pages

1. Go to repository "Settings"
2. Scroll down to "Pages" section
3. Under "Source", select "Deploy from a branch"
4. Choose "main" branch and click "Save"
5. Wait a few minutes for deployment

### 4. Set as Safari Start Page

1. Open Safari preferences
2. Go to "General" tab
3. Set "New windows open with" to "Homepage"
4. Enter your GitHub Pages URL (e.g., `https://your-username.github.io/your-repo-name`)
5. Enable "New tabs open with" and set to "Homepage"

## Manual Setup (Alternative)

If you don't want to use GitHub Secrets, you can manually add your API key:

1. Edit [`index.html`](index.html)
2. Find the line: `this.unsplashAccessKey = ''`
3. Replace with: `this.unsplashAccessKey = 'your_api_key_here'`
4. Commit and push changes

**Note:** This method exposes your API key in the source code, so GitHub Secrets is recommended.

## Features

-   🖼️ Auto-changing Unsplash backgrounds
-   ⏰ Configurable rotation interval (default: 30 minutes)
-   🎨 Smooth transitions with animated loading spinner
-   📱 Responsive design
-   🍎 Safari optimized
-   ☁️ GitHub Pages ready
-   🔒 Secure with GitHub Secrets

## Configuration

To change the rotation interval:

1. Edit [`index.html`](index.html)
2. Find `changeIntervalMinutes: 30`
3. Change the value to your preferred minutes
4. Commit and push changes

## Project Files

-   [`index.html`](index.html) - Main page with background display
-   [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) - GitHub Actions for deployment
-   [`README.md`](README.md) - Setup guide
-   [`LICENSE`](LICENSE) - MIT license
-   [`.gitignore`](.gitignore) - Standard ignore patterns

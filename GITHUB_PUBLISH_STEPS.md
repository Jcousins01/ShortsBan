# Step-by-Step: Publishing ShortsBan to GitHub

## Quick Overview
- **Time**: 15-20 minutes
- **Cost**: Free
- **Result**: Private repo with privacy policy page

---

## Step 1: Create GitHub Account (3 minutes)

1. Go to https://github.com
2. Click "Sign up" (top right)
3. Enter:
   - Username (e.g., `yourname` or `shortsban`)
   - Email address
   - Password
4. Verify your email (check inbox)
5. Complete any verification steps

✅ **Done when**: You can log into GitHub

---

## Step 2: Create New Repository (2 minutes)

1. Click the **"+"** icon (top right) → **"New repository"**
2. Fill in:
   - **Repository name**: `ShortsBan` (or `shortsban`)
   - **Description**: `Block YouTube Shorts automatically - Browser extension`
   - **Visibility**: 
     - ✅ **Private** (recommended - code stays private)
     - Or **Public** (if you want open source)
   - **DO NOT** check "Add a README file" (we'll add our own)
   - **DO NOT** add .gitignore or license yet
3. Click **"Create repository"**

✅ **Done when**: You see an empty repository page

---

## Step 3: Prepare Your Files Locally (5 minutes)

### Option A: Upload via GitHub Web Interface (Easiest)

1. On your new repo page, click **"uploading an existing file"**
2. Drag and drop these files from ONE extension folder (Firefox is fine):
   - `manifest.json`
   - `background.js`
   - `popup/` folder (with all files inside)
   - `icons/` folder (with all files inside)
3. Scroll down, add commit message: `Initial commit - ShortsBan extension`
4. Click **"Commit changes"**

### Option B: Use Git Command Line (If you have Git installed)

```bash
# Navigate to your extension folder
cd "/home/delta/Extentions/Firefox extention"

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - ShortsBan extension"

# Add remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/ShortsBan.git

# Push to GitHub
git branch -M main
git push -u origin main
```

✅ **Done when**: Files appear in your GitHub repository

---

## Step 4: Create README.md (3 minutes)

1. In your GitHub repo, click **"Add file"** → **"Create new file"**
2. Name it: `README.md`
3. Copy and paste this content (replace `YOUR_USERNAME` with your GitHub username):

```markdown
# ShortsBan

Block YouTube Shorts automatically. Prevents redirects to youtube.com/shorts and restores your previous page.

## ✨ Features

- 🚫 Automatically blocks YouTube Shorts URLs
- 🔄 Restores your previous page instantly
- 📊 Session tracking to see your progress
- ⚡ Lightweight and fast
- 🔒 Privacy-focused (no data collection)
- 💚 Free and open source

## 📥 Installation

### Firefox
[Install from Firefox Add-ons](https://addons.mozilla.org/firefox/addon/shortsban/)

### Chrome
[Install from Chrome Web Store](https://chrome.google.com/webstore/detail/shortsban/...)

### Microsoft Edge
[Install from Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/shortsban/...)

### Safari
[Install from Safari App Store](https://apps.apple.com/app/shortsban/...)

## 🎯 How It Works

When you click a YouTube Shorts link, ShortsBan automatically redirects you back to your previous page, preventing the distraction before it starts.

## 🔒 Privacy

ShortsBan doesn't collect, store, or transmit any personal data. All processing happens locally in your browser.

**Read our full [Privacy Policy](https://YOUR_USERNAME.github.io/ShortsBan/PRIVACY.html)**

## 🐛 Support

Found a bug? Have a feature request?

- [Open an issue](https://github.com/YOUR_USERNAME/ShortsBan/issues)
- Or email: [your-email@example.com]

## ☕ Donate

Support the developer and keep ShortsBan free:

[Donate via Stripe](https://donate.stripe.com/28o2ateSlccqakMfYZ)

## 📝 License

MIT License - feel free to use and modify

## 🙏 Credits

Created with ❤️ to help people stay focused
```

4. Scroll down, click **"Commit new file"**

✅ **Done when**: README.md appears in your repo

---

## Step 5: Create Privacy Policy Page (4 minutes)

1. Click **"Add file"** → **"Create new file"**
2. Name it: `PRIVACY.md`
3. Copy and paste this content:

```markdown
# ShortsBan Privacy Policy

**Last Updated:** [Today's Date]

## Data Collection

ShortsBan does **not** collect, store, or transmit any personal data.

## What We Don't Do

- ❌ We don't collect your browsing history
- ❌ We don't track your YouTube usage
- ❌ We don't send data to external servers
- ❌ We don't use analytics or tracking
- ❌ We don't store personal information

## Local Storage

ShortsBan only stores data locally in your browser:
- Session block count (resets when browser closes)
- Last block token (for notification management)

This data never leaves your device and is deleted when you close your browser.

## Permissions Explained

ShortsBan requires these permissions:

- **tabs**: To detect and block YouTube Shorts URLs
- **storage**: To track session statistics locally (never sent anywhere)
- **notifications**: To notify you when a Shorts link is blocked

## Third-Party Services

ShortsBan does not use any third-party analytics, tracking, or data collection services.

## Contact

If you have privacy concerns, please [open an issue](https://github.com/YOUR_USERNAME/ShortsBan/issues) or contact us.

## Changes to This Policy

We may update this privacy policy. Any changes will be posted here with an updated "Last Updated" date.

## Your Rights

You have the right to:
- Uninstall the extension at any time
- Clear all local data by uninstalling
- Review this policy at any time
```

4. Scroll down, click **"Commit new file"**

✅ **Done when**: PRIVACY.md appears in your repo

---

## Step 6: Enable GitHub Pages for Privacy Policy (2 minutes)

1. Go to your repo **Settings** (top menu)
2. Scroll down to **"Pages"** (left sidebar)
3. Under **"Source"**:
   - Select: **"Deploy from a branch"**
   - Branch: **`main`** (or `master`)
   - Folder: **`/ (root)`**
4. Click **"Save"**
5. Wait 1-2 minutes for GitHub to build your site

✅ **Done when**: You see a green checkmark and a URL like:
`https://YOUR_USERNAME.github.io/ShortsBan/`

---

## Step 7: Create Privacy Policy HTML Page (3 minutes)

1. Click **"Add file"** → **"Create new file"**
2. Name it: `PRIVACY.html`
3. Copy and paste this:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ShortsBan Privacy Policy</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem;
            line-height: 1.6;
            color: #333;
        }
        h1 { color: #d70022; }
        h2 { margin-top: 2rem; color: #1c1c1c; }
        a { color: #d70022; }
    </style>
</head>
<body>
    <h1>ShortsBan Privacy Policy</h1>
    
    <p><strong>Last Updated:</strong> [Today's Date]</p>
    
    <h2>Data Collection</h2>
    <p>ShortsBan does <strong>not</strong> collect, store, or transmit any personal data.</p>
    
    <h2>What We Don't Do</h2>
    <ul>
        <li>❌ We don't collect your browsing history</li>
        <li>❌ We don't track your YouTube usage</li>
        <li>❌ We don't send data to external servers</li>
        <li>❌ We don't use analytics or tracking</li>
        <li>❌ We don't store personal information</li>
    </ul>
    
    <h2>Local Storage</h2>
    <p>ShortsBan only stores data locally in your browser:</p>
    <ul>
        <li>Session block count (resets when browser closes)</li>
        <li>Last block token (for notification management)</li>
    </ul>
    <p>This data never leaves your device and is deleted when you close your browser.</p>
    
    <h2>Permissions Explained</h2>
    <p>ShortsBan requires these permissions:</p>
    <ul>
        <li><strong>tabs</strong>: To detect and block YouTube Shorts URLs</li>
        <li><strong>storage</strong>: To track session statistics locally (never sent anywhere)</li>
        <li><strong>notifications</strong>: To notify you when a Shorts link is blocked</li>
    </ul>
    
    <h2>Third-Party Services</h2>
    <p>ShortsBan does not use any third-party analytics, tracking, or data collection services.</p>
    
    <h2>Contact</h2>
    <p>If you have privacy concerns, please <a href="https://github.com/YOUR_USERNAME/ShortsBan/issues">open an issue</a> or contact us.</p>
    
    <h2>Changes to This Policy</h2>
    <p>We may update this privacy policy. Any changes will be posted here with an updated "Last Updated" date.</p>
    
    <hr>
    <p><a href="https://github.com/YOUR_USERNAME/ShortsBan">← Back to ShortsBan</a></p>
</body>
</html>
```

4. Replace `YOUR_USERNAME` with your actual GitHub username
5. Replace `[Today's Date]` with today's date
6. Click **"Commit new file"**

✅ **Done when**: PRIVACY.html appears in your repo

---

## Step 8: Update Your Extension Manifests (2 minutes)

Update the `homepage_url` in all 4 manifest.json files:

### Replace this line in all manifests:
```json
"homepage_url": "https://github.com/yourusername/shortsban"
```

### With this (replace YOUR_USERNAME):
```json
"homepage_url": "https://YOUR_USERNAME.github.io/ShortsBan/"
```

**Files to update:**
- `Firefox extention/manifest.json`
- `Chrome Extention/manifest.json`
- `Safari Extention/manifest.json`
- `Bing Extention/manifest.json`

✅ **Done when**: All manifests have your GitHub Pages URL

---

## Step 9: Test Your Privacy Policy Page (1 minute)

1. Wait 2-3 minutes after enabling GitHub Pages
2. Visit: `https://YOUR_USERNAME.github.io/ShortsBan/PRIVACY.html`
3. Verify it loads correctly
4. This is the URL you'll use for Chrome submission!

✅ **Done when**: Privacy policy page loads in browser

---

## ✅ You're Done!

### What You Now Have:
- ✅ GitHub repository with your code
- ✅ Privacy policy page (for Chrome submission)
- ✅ README with installation links
- ✅ Professional presence online

### Next Steps:
1. Update store listing URLs when you publish
2. Add installation links to README when extensions go live
3. Consider adding a CHANGELOG.md for version updates

### Your URLs:
- **Repository**: `https://github.com/YOUR_USERNAME/ShortsBan`
- **Privacy Policy**: `https://YOUR_USERNAME.github.io/ShortsBan/PRIVACY.html`
- **Homepage**: `https://YOUR_USERNAME.github.io/ShortsBan/`

---

## Troubleshooting

**GitHub Pages not working?**
- Wait 5-10 minutes (takes time to build)
- Check Settings → Pages → make sure it's enabled
- Verify branch is `main` or `master`

**Can't see files?**
- Make sure you committed them
- Check you're in the right repository
- Refresh the page

**Privacy policy 404?**
- Make sure PRIVACY.html is in the root folder
- Wait a few more minutes for GitHub to build
- Check the file name is exactly `PRIVACY.html`

---

## Optional: Make Repository Public Later

If you want to make it public later:
1. Go to Settings → scroll to bottom
2. Click "Change visibility" → "Make public"
3. Your code will be visible to everyone

You can always keep it private if you prefer!

---

**Need help?** GitHub has great documentation: https://docs.github.com

Good luck! 🚀



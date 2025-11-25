# Quick GitHub Setup for ShortsBan (10 Minutes)

## Why Set Up GitHub?

### Immediate Benefits:
1. **Privacy Policy Hosting** - Chrome may require this
2. **User Trust** - Shows you're a real developer
3. **Support Channel** - Users can report bugs via Issues
4. **SEO** - Your extension becomes discoverable via search
5. **Professional** - Makes your extension look established

### Future Benefits:
- Update announcements
- Feature requests
- User testimonials
- Analytics tracking
- Donation thank-yous

---

## 10-Minute Setup

### Step 1: Create GitHub Account (2 min)
1. Go to https://github.com
2. Sign up (free)
3. Verify email

### Step 2: Create Repository (1 min)
1. Click "+" → "New repository"
2. Name: `ShortsBan` (or `shortsban`)
3. Description: "Block YouTube Shorts automatically - Browser extension"
4. Make it **Public** (so people can find it)
5. Don't initialize with README (we'll add our own)
6. Click "Create repository"

### Step 3: Add Files (5 min)

Create these files in your repo:

#### README.md
```markdown
# ShortsBan

Block YouTube Shorts automatically. Prevents redirects to youtube.com/shorts and restores your previous page.

## Features

- 🚫 Automatically blocks YouTube Shorts URLs
- 🔄 Restores your previous page instantly
- 📊 Session tracking to see your progress
- ⚡ Lightweight and fast
- 🔒 Privacy-focused (no data collection)
- 💚 Free and open source

## Installation

### Firefox
[Link to Firefox Add-ons store]

### Chrome
[Link to Chrome Web Store]

### Edge
[Link to Edge Add-ons store]

### Safari
[Link to Safari App Store]

## How It Works

When you click a YouTube Shorts link, ShortsBan automatically redirects you back to your previous page, preventing the distraction before it starts.

## Privacy

ShortsBan doesn't collect, store, or transmit any personal data. All processing happens locally in your browser.

## Support

Found a bug? Have a feature request? [Open an issue](https://github.com/YOUR_USERNAME/ShortsBan/issues)

## Donate

Support the developer and keep ShortsBan free: [Donate via Stripe](https://donate.stripe.com/28o2ateSlccqakMfYZ)

## License

MIT License - feel free to use and modify
```

#### PRIVACY.md (Simple Privacy Policy)
```markdown
# ShortsBan Privacy Policy

**Last Updated:** [Date]

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

This data never leaves your device.

## Permissions

ShortsBan requires these permissions:
- **tabs**: To detect and block YouTube Shorts URLs
- **storage**: To track session statistics locally
- **notifications**: To notify you when a Shorts link is blocked

## Contact

If you have privacy concerns, please [open an issue](https://github.com/YOUR_USERNAME/ShortsBan/issues)

## Changes

We may update this privacy policy. Changes will be posted here.
```

### Step 4: Enable GitHub Pages (2 min)
1. Go to repo Settings → Pages
2. Source: "Deploy from a branch"
3. Branch: `main` (or `master`)
4. Folder: `/ (root)`
5. Click Save
6. Your site will be at: `https://YOUR_USERNAME.github.io/ShortsBan/`

### Step 5: Update Your Manifests
Update `homepage_url` in all manifest.json files:
```json
"homepage_url": "https://YOUR_USERNAME.github.io/ShortsBan/"
```

Or use the GitHub repo URL:
```json
"homepage_url": "https://github.com/YOUR_USERNAME/ShortsBan"
```

---

## What You Get

✅ Privacy policy URL for Chrome submission  
✅ Professional appearance  
✅ User support channel (GitHub Issues)  
✅ SEO benefits  
✅ Update announcements  
✅ Free hosting (GitHub Pages)  

---

## Optional: Add More Pages Later

- `CHANGELOG.md` - Version history
- `CONTRIBUTING.md` - How others can help
- `LICENSE` - MIT License file
- Screenshots folder
- Demo GIF/video

---

## Time Investment

- **Initial Setup**: 10 minutes
- **Maintenance**: Minimal (just update when you release new versions)
- **Cost**: $0 (completely free)

---

## Pro Tip

You can always start simple and expand later. Even a basic README and privacy policy is better than nothing!



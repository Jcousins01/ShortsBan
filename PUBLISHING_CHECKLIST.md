# ShortsBan Publishing Checklist

## Pre-Publication Checklist

### ✅ Code Ready
- [x] All extensions ported (Firefox, Chrome, Safari, Edge)
- [x] Stripe donation link integrated
- [x] Responsive design implemented
- [x] Accessibility features added
- [x] SEO optimizations included
- [ ] Homepage URL updated (currently placeholder)
- [ ] All files tested in each browser

### ⚠️ Before Publishing - Update These

1. **Homepage URL** (in all manifest.json files):
   - Current: `"https://github.com/yourusername/shortsban"`
   - Update to: Your actual GitHub repo or website URL
   - Or remove if you don't have one yet

2. **Test Each Extension**:
   - Load unpacked extension in each browser
   - Verify blocking works
   - Check popup displays correctly
   - Test donation link opens
   - Verify notifications work

---

## Firefox Add-ons (addons.mozilla.org)

### Requirements
- Firefox Developer Account (free)
- Valid email address
- Extension packaged as .zip or .xpi

### Steps
1. **Create Account**: https://addons.mozilla.org/developers/
2. **Package Extension**:
   - Zip the Firefox extension folder (without parent folder)
   - Or use `web-ext build` command
3. **Submit**:
   - Go to Developer Hub → Submit a New Add-on
   - Upload your .zip file
   - Fill out listing details:
     - Name: ShortsBan
     - Summary: Block YouTube Shorts automatically
     - Description: Detailed description (can use manifest description)
     - Categories: Productivity, Privacy & Security
     - Tags: youtube, shorts, blocker, productivity, focus
     - Screenshots: Take screenshots of popup
     - Icon: Use icon-96.png
4. **Review Process**: Usually 1-3 days
5. **Publish**: Once approved, it's live!

### Firefox-Specific Notes
- Manifest V2 is still supported
- Review process is thorough
- Need to explain permissions clearly

---

## Chrome Web Store (chrome.google.com/webstore)

### Requirements
- Google Developer Account ($5 one-time fee)
- Valid payment method
- Extension packaged as .zip

### Steps
1. **Create Account**: https://chrome.google.com/webstore/devconsole
2. **Pay Registration Fee**: $5 one-time (if not already paid)
3. **Package Extension**:
   - Zip the Chrome extension folder
   - Make sure manifest.json is at root
4. **Submit**:
   - Go to Chrome Web Store Developer Dashboard
   - Click "New Item"
   - Upload .zip file
   - Fill out listing:
     - Name: ShortsBan
     - Detailed description (use manifest description + more)
     - Category: Productivity
     - Language: English
     - Privacy practices: Required
     - Screenshots: At least 1 (1280x800 or 640x400)
     - Promotional images: Optional but recommended
     - Small tile: 440x280
     - Icon: 128x128 (use icon-96.png scaled up)
5. **Review Process**: Usually 1-7 days
6. **Publish**: Once approved!

### Chrome-Specific Notes
- Manifest V3 required
- Privacy policy may be required
- More strict review process
- Need to explain host_permissions

---

## Safari App Store (developer.apple.com)

### Requirements
- Apple Developer Account ($99/year)
- macOS for development/testing
- Xcode (for building)

### Steps
1. **Create Account**: https://developer.apple.com/programs/
2. **Pay Annual Fee**: $99/year
3. **Build Extension**:
   - Use Xcode to create Safari App Extension
   - Convert your extension to Safari format
   - Or use Safari Web Extension Converter tool
4. **Submit via App Store Connect**:
   - Create app listing
   - Upload build
   - Fill out metadata
   - Submit for review
5. **Review Process**: Usually 1-3 days
6. **Publish**: Once approved!

### Safari-Specific Notes
- Most complex process
- Requires macOS and Xcode
- Annual developer fee
- May need to rebuild for Safari format
- Consider using Safari Web Extension Converter

---

## Microsoft Edge Add-ons (microsoftedge.microsoft.com/addons)

### Requirements
- Microsoft Partner Center account (free)
- Valid email address
- Extension packaged as .zip

### Steps
1. **Create Account**: https://partner.microsoft.com/dashboard
2. **Package Extension**:
   - Zip the Bing/Edge extension folder
   - Same structure as Chrome
3. **Submit**:
   - Go to Partner Center → Edge Add-ons
   - Click "Create new extension"
   - Upload .zip file
   - Fill out listing:
     - Name: ShortsBan
     - Description: Detailed description
     - Category: Productivity
     - Screenshots: At least 1
     - Icon: Use icon-96.png
4. **Review Process**: Usually 1-5 days
5. **Publish**: Once approved!

### Edge-Specific Notes
- Very similar to Chrome
- Manifest V3
- Usually faster review than Chrome
- Good alternative if Chrome is slow

---

## Assets Needed for All Stores

### Required
- [x] Extension icon (48x48, 96x96) ✅
- [ ] Screenshots (at least 1, preferably 3-5)
  - Popup screenshot
  - Extension in action
  - Settings/features
- [ ] Store listing description (longer than manifest)
- [ ] Privacy policy (may be required)

### Recommended
- [ ] Promotional images
- [ ] Video demo
- [ ] Support email/website
- [ ] GitHub repository link

---

## Screenshot Guidelines

### What to Screenshot
1. **Popup Interface**: Show the extension popup with session count
2. **In Action**: Show before/after (YouTube page → blocked)
3. **Notification**: Show notification when Shorts is blocked
4. **Settings**: If you add settings later

### Screenshot Sizes
- **Chrome**: 1280x800 or 640x400
- **Firefox**: 1200x675 or 600x450
- **Edge**: 1280x800
- **Safari**: Varies

---

## Store Listing Description Template

```
ShortsBan automatically blocks YouTube Shorts and prevents redirects to youtube.com/shorts, helping you stay focused and maintain your YouTube browsing flow.

✨ Features:
• Automatically blocks YouTube Shorts URLs
• Restores your previous page instantly
• Session tracking to see your progress
• Lightweight and fast
• Privacy-focused (no data collection)
• Free and open source

🎯 Perfect for:
• Students who need to focus
• Professionals avoiding distractions
• Anyone who wants to control their YouTube experience

🔒 Privacy:
ShortsBan doesn't collect, store, or transmit any personal data. All processing happens locally in your browser.

💡 How it works:
When you click a YouTube Shorts link, ShortsBan automatically redirects you back to your previous page, preventing the distraction before it starts.

Support the developer and keep ShortsBan free: [Your donation link]
```

---

## Quick Start Publishing Order

1. **Edge** (Easiest, fastest approval)
2. **Firefox** (Free, good community)
3. **Chrome** (Largest audience, $5 fee)
4. **Safari** (Most complex, $99/year)

---

## Post-Publication

- [ ] Monitor reviews and ratings
- [ ] Respond to user feedback
- [ ] Track download/install numbers
- [ ] Monitor donation link clicks
- [ ] Update based on feedback
- [ ] Consider adding features users request

---

## Need Help?

- **Firefox**: https://extensionworkshop.com/documentation/publish/
- **Chrome**: https://developer.chrome.com/docs/webstore/publish
- **Edge**: https://docs.microsoft.com/en-us/microsoft-edge/extensions-chromium/publish/
- **Safari**: https://developer.apple.com/safari/extensions/

Good luck with your launch! 🚀



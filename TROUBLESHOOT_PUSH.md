# Troubleshooting GitHub Push - 403 Error

## The Issue

Getting "Permission denied" (403 error) usually means:
1. Token doesn't have `repo` scope
2. Token expired or was revoked
3. Repository settings blocking access

## Solution 1: Verify Token Permissions

1. Go to: https://github.com/settings/tokens
2. Find your token (named "Cursor Git Access" or similar)
3. Check if it has **`repo`** scope checked
4. If not, you need to create a new token with `repo` scope

## Solution 2: Create New Token with Correct Permissions

1. Go to: https://github.com/settings/tokens/new
2. **IMPORTANT**: Under "Select scopes", check:
   - ✅ **`repo`** (this gives full repository access)
   - This is the most important one!
3. Generate new token
4. Copy the new token
5. Try pushing again

## Solution 3: Upload via Web Interface (Easiest Alternative)

If tokens keep causing issues, upload files directly:

1. Go to: https://github.com/Jcousins01/ShortsBan
2. Click **"uploading an existing file"** (or "Add file" → "Upload files")
3. Drag and drop all files from your Firefox extension folder:
   - `background.js`
   - `manifest.json`
   - `popup/` folder
   - `icons/` folder
   - `.gitignore`
4. Scroll down, add commit message: `Initial commit - ShortsBan extension`
5. Click **"Commit changes"**

This bypasses Git authentication entirely!

## Solution 4: Check Repository Settings

1. Go to: https://github.com/Jcousins01/ShortsBan/settings
2. Check if repository is set to **Private** or **Public**
3. Make sure you're the owner (Jcousins01)

## Quick Test

Try this to test your token:
```bash
curl -H "Authorization: token YOUR_TOKEN" https://api.github.com/user
```

If it returns your user info, token works. If it returns an error, token has issues.

---

**Easiest solution right now**: Upload files via web interface (Solution 3) - no authentication needed!



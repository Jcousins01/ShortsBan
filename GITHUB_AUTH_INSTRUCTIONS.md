# GitHub Authentication - Quick Guide

## Option 1: Personal Access Token (Recommended)

### Step 1: Create Token on GitHub

1. Go to: https://github.com/settings/tokens
2. Click **"Generate new token"** → **"Generate new token (classic)"**
3. Fill in:
   - **Note**: `Cursor Git Access` (or any name)
   - **Expiration**: Choose 90 days or No expiration
   - **Select scopes**: Check **`repo`** (this gives full access to repositories)
4. Click **"Generate token"** at the bottom
5. **IMPORTANT**: Copy the token immediately (you won't see it again!)
   - It will look like: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`

### Step 2: Use Token to Push

When you run `git push`, it will ask for:
- **Username**: `Jcousins01`
- **Password**: Paste your Personal Access Token (NOT your GitHub password)

---

## Option 2: Use GitHub CLI (Easier - if installed)

If you have GitHub CLI installed:

```bash
gh auth login
```

Follow the prompts to authenticate.

---

## Option 3: Configure Git Credential Helper (One-time setup)

After you push once with token, you can save it:

```bash
git config --global credential.helper store
```

Then when you push, enter your token once, and it will be saved.

---

## Quick Push Command

Once you have your token, run:

```bash
cd "/home/delta/Extentions/Firefox extention"
git push -u origin main
```

When prompted:
- Username: `Jcousins01`
- Password: `YOUR_PERSONAL_ACCESS_TOKEN`

---

## Alternative: Use SSH (More Secure, One-time Setup)

If you prefer SSH (no token needed each time):

1. Generate SSH key:
```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
```

2. Add to GitHub:
   - Copy public key: `cat ~/.ssh/id_ed25519.pub`
   - Go to: https://github.com/settings/keys
   - Click "New SSH key"
   - Paste key and save

3. Change remote to SSH:
```bash
git remote set-url origin git@github.com:Jcousins01/ShortsBan.git
```

4. Push:
```bash
git push -u origin main
```

---

**Easiest for now**: Create Personal Access Token and use it when pushing!



# Setup Git and Push to GitHub from Cursor

## Step 1: Install Git (if not installed)

Open a terminal and run:

```bash
sudo yum install -y git
```

Enter your password when prompted.

Verify installation:
```bash
git --version
```

---

## Step 2: Configure Git (Optional - But Recommended)

**You can skip this**, but Git will ask for it when you make your first commit.

Set your name and email (can be anything - doesn't have to be real):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

**Note:** 
- The name/email can be anything (doesn't have to be your real name)
- It's visible in commit history (but only if someone looks at commits)
- For private repos, it matters less
- If you skip this, Git will prompt you on first commit anyway

---

## Step 3: Create GitHub Repository

### Option A: Via GitHub Website (Easiest)

1. Go to https://github.com and log in
2. Click **"+"** → **"New repository"**
3. Name: `ShortsBan`
4. Description: `Block YouTube Shorts automatically - Browser extension`
5. Choose **Private** (recommended) or **Public**
6. **DO NOT** initialize with README, .gitignore, or license
7. Click **"Create repository"**
8. **Copy the repository URL** (you'll need it in Step 4)
   - It will look like: `https://github.com/YOUR_USERNAME/ShortsBan.git`

### Option B: Via GitHub CLI (if you install it later)

```bash
gh repo create ShortsBan --private --description "Block YouTube Shorts automatically"
```

---

## Step 4: Initialize Git in Your Extension Folder

We'll use the **Firefox extension** folder as the base (you can add others later):

```bash
cd "/home/delta/Extentions/Firefox extention"
git init
```

---

## Step 5: Create .gitignore (Optional but Recommended)

Create a `.gitignore` file to exclude unnecessary files:

```bash
cat > .gitignore << 'EOF'
# IDE files
*.code-workspace
.vscode/
.idea/

# OS files
.DS_Store
Thumbs.db

# Logs
*.log

# Temporary files
*.tmp
*.temp
EOF
```

---

## Step 6: Add Files and Make First Commit

```bash
# Add all files
git add .

# Make initial commit
git commit -m "Initial commit - ShortsBan extension v1.0.1"
```

---

## Step 7: Connect to GitHub Repository

Replace `YOUR_USERNAME` with your actual GitHub username:

```bash
git remote add origin https://github.com/YOUR_USERNAME/ShortsBan.git
```

---

## Step 8: Push to GitHub

```bash
# Set main branch
git branch -M main

# Push to GitHub
git push -u origin main
```

You'll be prompted for your GitHub username and password (or personal access token).

---

## Step 9: Set Up Authentication

GitHub no longer accepts passwords. You need a **Personal Access Token**:

### Create Personal Access Token:

1. Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Click **"Generate new token (classic)"**
3. Name it: `Cursor Git Access`
4. Select scopes: Check **`repo`** (full control of private repositories)
5. Click **"Generate token"**
6. **COPY THE TOKEN** (you won't see it again!)

### Use Token When Pushing:

When you run `git push`, use:
- **Username**: Your GitHub username
- **Password**: Your Personal Access Token (not your GitHub password)

---

## Step 10: Add Other Extension Folders (Optional)

If you want to include all extensions in one repo:

```bash
cd "/home/delta/Extentions"

# Create .gitignore at root
cat > .gitignore << 'EOF'
*.code-workspace
.DS_Store
Thumbs.db
*.log
EOF

# Initialize git at root level
git init

# Add all extension folders
git add "Firefox extention/"
git add "Chrome Extention/"
git add "Safari Extention/"
git add "Bing Extention/"

# Commit
git commit -m "Add all browser extension versions"

# Push
git push origin main
```

---

## Quick Reference Commands

```bash
# Check status
git status

# Add files
git add .

# Commit changes
git commit -m "Your commit message"

# Push to GitHub
git push

# Pull from GitHub
git pull

# View remote
git remote -v
```

---

## Troubleshooting

### "Permission denied" error:
- Make sure you're using Personal Access Token, not password
- Check token has `repo` scope

### "Repository not found":
- Verify repository name is correct
- Check you have access (if private repo)
- Make sure repository exists on GitHub

### "Authentication failed":
- Generate new Personal Access Token
- Make sure token hasn't expired

---

## Next Steps After Pushing

1. Add README.md (see GITHUB_PUBLISH_STEPS.md)
2. Add PRIVACY.md and PRIVACY.html
3. Enable GitHub Pages
4. Update manifest.json files with GitHub Pages URL

---

**Ready to start?** Run the commands in order, and let me know if you hit any issues!


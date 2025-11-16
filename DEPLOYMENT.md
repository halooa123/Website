# Quick Deployment Guide

## Upload to GitHub Pages (5 minutes)

### 1. Create GitHub Repository
- Go to https://github.com/new
- Name: `jf-footbath-massage` (or your choice)
- Make it **Public**
- Click **Create repository**

### 2. Upload Files via Command Line

```bash
# Navigate to your project folder
cd C:\Users\awsx3\massage-website

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit"

# Add remote (replace YOUR_USERNAME and REPO_NAME)
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages
1. Go to your repository on GitHub
2. **Settings** → **Pages**
3. Source: **main** branch, **/ (root)**
4. Click **Save**
5. Wait 2-3 minutes
6. Visit: `https://YOUR_USERNAME.github.io/REPO_NAME/`

---

## Add Custom Domain (.com)

### Step 1: Buy Domain
- Purchase from Namecheap, Google Domains, or GoDaddy
- Example: `jffootbathmassage.com`

### Step 2: Configure DNS
In your domain registrar, add these **A records**:

```
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153
```

### Step 3: Add Domain to GitHub
1. Repository → **Settings** → **Pages**
2. Custom domain: `yourdomain.com`
3. Check **Enforce HTTPS**
4. Save

### Step 4: Create CNAME File
Create `CNAME` file (no extension) with:
```
yourdomain.com
```

Then:
```bash
git add CNAME
git commit -m "Add custom domain"
git push
```

### Step 5: Wait
- DNS propagation: 24-48 hours
- Check status: https://dnschecker.org
- Your site will work at `https://yourdomain.com`

---

## Need Help?

- GitHub Pages Docs: https://docs.github.com/en/pages
- Custom Domain Help: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site


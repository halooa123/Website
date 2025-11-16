# Serenity Massage Website

A beautiful, modern, and responsive website for a massage therapy business, ready to deploy on GitHub Pages.

## Features

- 🎨 Modern and elegant design
- 📱 Fully responsive (mobile, tablet, desktop)
- 🖼️ High-quality images from Unsplash
- ⚡ Smooth animations and transitions
- 📋 Contact form for booking requests
- 🧭 Smooth scrolling navigation
- ♿ Accessible and SEO-friendly

## Technologies Used

- HTML5
- CSS3 (with CSS Grid and Flexbox)
- Vanilla JavaScript
- Google Fonts (Playfair Display & Inter)
- Unsplash (for free stock photos)

## Getting Started

### Local Development

1. Clone or download this repository
2. Open `index.html` in your web browser
3. That's it! No build process required.

### Deploying to GitHub Pages

#### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in (or create an account)
2. Click the **+** icon in the top right corner and select **New repository**
3. Name your repository (e.g., `jf-footbath-massage` or `massage-website`)
4. Choose **Public** (required for free GitHub Pages)
5. **DO NOT** initialize with README, .gitignore, or license (we already have files)
6. Click **Create repository**

#### Step 2: Push Your Code to GitHub

Open PowerShell or Terminal in your project folder and run:

```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Create your first commit
git commit -m "Initial commit - JF FOOT BATH Massage website"

# Rename branch to main (if needed)
git branch -M main

# Add your GitHub repository as remote (replace with your actual repo URL)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Push to GitHub
git push -u origin main
```

**Note:** Replace `YOUR_USERNAME` and `YOUR_REPO_NAME` with your actual GitHub username and repository name.

#### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** (top menu)
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select **main** branch and `/ (root)` folder
5. Click **Save**
6. Wait a few minutes for GitHub to build your site
7. Your site will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

**Example:** If your username is `johndoe` and repo is `massage-website`, your site will be at:
`https://johndoe.github.io/massage-website/`

---

## Setting Up a Custom Domain (.com)

### Step 1: Purchase a Domain

1. Buy a domain from a registrar like:
   - [Namecheap](https://www.namecheap.com)
   - [Google Domains](https://domains.google)
   - [GoDaddy](https://www.godaddy.com)
   - [Cloudflare](https://www.cloudflare.com/products/registrar)

2. Choose your domain (e.g., `jffootbathmassage.com`)

### Step 2: Configure DNS Records

In your domain registrar's DNS settings, add these records:

**Option A: Using A Records (Recommended)**
- Type: `A`
- Name: `@` (or leave blank for root domain)
- Value: `185.199.108.153`
- TTL: `3600` (or default)

- Type: `A`
- Name: `@`
- Value: `185.199.109.153`
- TTL: `3600`

- Type: `A`
- Name: `@`
- Value: `185.199.110.153`
- TTL: `3600`

- Type: `A`
- Name: `@`
- Value: `185.199.111.153`
- TTL: `3600`

**Option B: Using CNAME (For www subdomain)**
- Type: `CNAME`
- Name: `www`
- Value: `YOUR_USERNAME.github.io`
- TTL: `3600`

**Note:** Replace `YOUR_USERNAME` with your actual GitHub username.

### Step 3: Add Custom Domain to GitHub Pages

1. Go to your GitHub repository
2. Click **Settings** → **Pages**
3. Under **Custom domain**, enter your domain (e.g., `jffootbathmassage.com`)
4. Check **Enforce HTTPS** (recommended)
5. Click **Save**

### Step 4: Create CNAME File (Optional but Recommended)

Create a file named `CNAME` (no extension) in your project root with your domain:

```
jffootbathmassage.com
```

Then commit and push:
```bash
git add CNAME
git commit -m "Add custom domain CNAME"
git push
```

### Step 5: Wait for DNS Propagation

- DNS changes can take 24-48 hours to propagate globally
- You can check propagation status at: [whatsmydns.net](https://www.whatsmydns.net)
- Once DNS is updated, your site will be accessible at your custom domain

### Step 6: Verify SSL Certificate

GitHub automatically provides SSL certificates for custom domains. After DNS propagation:
1. Go to repository **Settings** → **Pages**
2. Ensure **Enforce HTTPS** is checked
3. Your site will be available at `https://yourdomain.com`

---

## Troubleshooting

### GitHub Pages Not Loading
- Wait 5-10 minutes after enabling Pages
- Check repository is **Public**
- Verify `index.html` is in the root directory
- Check repository **Settings** → **Pages** for any error messages

### Custom Domain Not Working
- Verify DNS records are correct (use [DNS Checker](https://dnschecker.org))
- Wait 24-48 hours for DNS propagation
- Ensure CNAME file is in repository root
- Check GitHub Pages settings show your domain
- Try accessing both `http://` and `https://` versions

### Images Not Loading
- Verify image paths are correct (relative paths work best)
- Check that `images/` folder is included in repository
- Ensure image file names match exactly (case-sensitive)

## Customization

### Update Business Information

Edit the following in `index.html`:
- Business name (search for "Serenity Massage")
- Contact information (phone, email, address)
- Business hours
- Service descriptions and prices

### Change Colors

Edit the CSS variables in `styles.css`:
```css
:root {
    --primary-color: #8B7355;    /* Main brand color */
    --secondary-color: #D4C4B0;  /* Secondary color */
    --accent-color: #C9A96B;     /* Accent color */
}
```

### Update Images

All images are from Unsplash. To change them:
1. Visit [Unsplash](https://unsplash.com)
2. Search for massage/spa related images
3. Copy the image URL
4. Replace the `src` attribute in the `<img>` tags

## File Structure

```
massage-website/
├── index.html      # Main HTML file
├── styles.css      # All styling
├── script.js       # JavaScript functionality
└── README.md       # This file
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## License

This project is open source and available for personal and commercial use.

## Credits

- Images: [Unsplash](https://unsplash.com)
- Fonts: [Google Fonts](https://fonts.google.com)

---

**Note:** The contact form currently shows an alert message. To make it functional, you'll need to:
- Set up a backend service (e.g., Formspree, Netlify Forms, or your own server)
- Update the form submission handler in `script.js`


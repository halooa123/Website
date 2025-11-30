# Fix HTTPS Issues on GitHub Pages

## If Using GitHub.io Domain (username.github.io)

GitHub Pages automatically provides HTTPS for `*.github.io` domains. If you're seeing HTTP:

1. **Clear your browser cache** - Sometimes browsers cache the HTTP version
2. **Try accessing with https:// explicitly** - Type `https://yourusername.github.io/repo-name`
3. **Wait a few minutes** - HTTPS may take 5-10 minutes to activate after first deployment
4. **Check repository settings**:
   - Go to Settings → Pages
   - Ensure the site is published
   - Look for any warnings or errors

## If Using Custom Domain (.com)

### Step 1: Enable HTTPS in GitHub

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under **Custom domain**, you should see your domain
4. **Check the box "Enforce HTTPS"** (this may take a few minutes to appear)
5. Wait 10-30 minutes for GitHub to issue the SSL certificate

### Step 2: Verify DNS Settings

Make sure your DNS A records are correct:
- `185.199.108.153`
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

### Step 3: Check CNAME File

Ensure you have a `CNAME` file in your repository root with:
```
yourdomain.com
```

Then commit and push:
```bash
git add CNAME
git commit -m "Add CNAME for HTTPS"
git push
```

### Step 4: Force HTTPS Redirect

If HTTPS still doesn't work, you can add this to your HTML `<head>` section to force HTTPS redirects.

## Common Issues

### "Enforce HTTPS" checkbox is grayed out
- Wait 24-48 hours after adding custom domain
- Ensure DNS is properly configured
- Check that CNAME file exists in repository

### Mixed Content Warnings
- Make sure all images and resources use HTTPS or relative paths
- Check browser console for mixed content errors

### Certificate Not Issued
- GitHub issues certificates automatically
- Can take up to 24 hours after DNS propagation
- Verify domain ownership in GitHub Pages settings

## Quick Test

1. Visit: `https://yourdomain.com` (with https://)
2. Check browser padlock icon
3. If it shows "Not Secure", wait longer or check DNS settings


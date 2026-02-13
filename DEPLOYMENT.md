# Deployment Guide

## Quick Start - GitHub Pages

### Step 1: Create GitHub Repository
1. Go to [github.com/new](https://github.com/new)
2. Create a new repository named: `yourusername.github.io`
3. Make sure it's **public**

### Step 2: Clone & Push Your Site
```bash
# Clone the repository
git clone https://github.com/yourusername/yourusername.github.io.git
cd yourusername.github.io

# Copy all files from this Profile folder to the repository
# Then commit and push
git add .
git commit -m "Initial portfolio site"
git push origin main
```

### Step 3: Verify Deployment
Your site will be live at: `https://yourusername.github.io`

---

## Custom Domain Setup (Optional)

### Step 1: Purchase Domain
Get a domain from:
- GoDaddy
- Namecheap
- Google Domains
- Cloudflare

### Step 2: Create CNAME File
Create a file named `CNAME` in the root directory:
```
your-custom-domain.com
```

### Step 3: Configure DNS
Point your domain's DNS records to GitHub:
- Type: A
- Name: @
- Value: Use GitHub's IP addresses (see [GitHub documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site))

### Step 4: Update GitHub Settings
1. Go to your repository Settings
2. Pages section
3. Enter your custom domain
4. Enable HTTPS

---

## Alternative Hosting Options

### Netlify
1. Connect your GitHub repository
2. Set build command: (leave empty)
3. Set publish directory: `/` (root)
4. Deploy!

### Vercel
1. Import your GitHub repository
2. Vercel auto-detects static site
3. Deploy!

### AWS S3 + CloudFront
1. Create S3 bucket
2. Enable static website hosting
3. Upload files
4. Set up CloudFront distribution

---

## SEO Optimization

Add meta tags to `index.html` `<head>`:

```html
<meta name="description" content="Zhang Xu - Researcher in Flexible Electronics and Neuromorphic Computing">
<meta name="keywords" content="flexible electronics, neuromorphic computing, wearables, research">
<meta name="author" content="Zhang Xu">

<!-- Open Graph for social sharing -->
<meta property="og:title" content="Zhang Xu | Researcher">
<meta property="og:description" content="Portfolio of research in flexible electronics and neuromorphic computing">
<meta property="og:type" content="website">
<meta property="og:url" content="https://yourdomain.com">
<meta property="og:image" content="https://yourdomain.com/assets/preview.png">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Zhang Xu | Researcher">
<meta name="twitter:description" content="Portfolio of research in flexible electronics and neuromorphic computing">
```

---

## Updating Your Site

### Local Development
1. Edit files locally
2. Test in browser
3. Push changes:
```bash
git add .
git commit -m "Update: description of changes"
git push origin main
```

### Automatic Deployment
GitHub Pages redeploys automatically when you push to your main branch.

---

## Troubleshooting

### Site Not Showing
- [ ] Repository name is correct: `yourusername.github.io`
- [ ] Repository is public
- [ ] Files are in root directory
- [ ] Wait 2-5 minutes for GitHub to process

### Custom Domain Not Working
- [ ] CNAME file exists with correct domain
- [ ] DNS records are correctly configured
- [ ] HTTPS is enabled in GitHub settings

### Performance Issues
- [ ] Reduce image sizes
- [ ] Enable gzip compression
- [ ] Use CDN for static assets

---

## Security Best Practices

✓ Always use HTTPS
✓ Keep dependencies updated
✓ Don't commit sensitive information
✓ Regular backups

---

For detailed GitHub Pages documentation, visit:
https://docs.github.com/en/pages

For help with issues, GitHub Support: https://support.github.com

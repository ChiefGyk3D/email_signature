# Netlify Setup Guide

This guide will help you set up automatic deployments to Netlify for your email signatures.

## Quick Setup (Netlify Auto-Deploy)

Since you've already linked Netlify to this repo, deployments should happen automatically! Every time you push to the `main` branch, Netlify will automatically rebuild and deploy.

### What's Already Configured:

1. ✅ **netlify.toml** - Configuration file for build settings and redirects
2. ✅ **index.html** - Landing page to access both signature versions
3. ✅ **GitHub Actions** - Workflow for automated deployments (optional enhancement)

### Your Signatures Are Available At:

- **Landing Page**: `https://your-site-name.netlify.app/`
- **Desktop Signature**: `https://your-site-name.netlify.app/signature.html`
- **Mobile Signature**: `https://your-site-name.netlify.app/mobile`

## Optional: GitHub Actions Setup

If you want GitHub Actions to handle deployments (in addition to Netlify's auto-deploy):

1. Go to your Netlify site settings
2. Get your **Site ID** from Site Settings → General → Site details
3. Create a **Personal Access Token** from User Settings → Applications → Personal access tokens
4. Add these as GitHub Secrets:
   - Go to your GitHub repo → Settings → Secrets and variables → Actions
   - Add `NETLIFY_AUTH_TOKEN` (your personal access token)
   - Add `NETLIFY_SITE_ID` (your site ID)

## How It Works

### Automatic Updates:
1. Make changes to `signature.html` or `mobile_signature`
2. Commit and push to the `main` branch
3. Netlify automatically detects the change and redeploys
4. Your signatures are live in ~30 seconds!

### Testing Changes:
- Create a branch and open a PR
- Netlify will create a **deploy preview** 
- Test your changes before merging to main

## Using Your Signature

1. Visit your Netlify URL (e.g., `https://chiefgyk3d-signature.netlify.app`)
2. Click either "Desktop" or "Mobile" version
3. Press Ctrl+A (or Cmd+A) to select all
4. Copy with Ctrl+C (or Cmd+C)
5. Paste into your email client's signature editor

## Custom Domain (Optional)

Want a custom domain like `signature.chiefgyk3d.com`?

1. Go to Netlify → Domain Settings → Add custom domain
2. Add your domain/subdomain
3. Update your DNS with the provided records
4. SSL certificate is automatically provisioned!

## Troubleshooting

### Icons not loading?
- Check that the `icons/` folder is committed to the repo
- Verify the GitHub raw URLs are correct in your HTML

### Changes not showing?
- Clear your browser cache (Ctrl+Shift+R or Cmd+Shift+R)
- Check Netlify deploy logs for errors
- Ensure you pushed to the `main` branch

### Email client stripping styles?
- Some email clients (like Gmail) strip certain CSS
- Test your signature in multiple email clients
- The inline styles should work in most cases

## Need Help?

- Check Netlify deploy logs: Site → Deploys
- View build logs for errors
- Test locally by opening HTML files in a browser

---

**Pro Tip**: Bookmark your Netlify URL for easy access whenever you need to copy your signature!

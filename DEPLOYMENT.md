# Team Piratez Racing - Vercel Deployment Guide

## Prerequisites

Before deploying to Vercel, ensure you have:
1. A [GitHub](https://github.com) account
2. A [Vercel](https://vercel.com) account (sign up with GitHub)
3. Git installed on your computer

## Deployment Steps

### Method 1: Deploy via Vercel Dashboard (Easiest)

1. **Push to GitHub**
   ```bash
   # Navigate to your project folder
   cd "d:\Website Piratez"
   
   # Initialize Git (if not already done)
   git init
   
   # Add all files
   git add .
   
   # Commit
   git commit -m "Initial commit: Team Piratez Racing website"
   
   # Create a new repository on GitHub and push
   git remote add origin https://github.com/YOUR_USERNAME/team-piratez-racing.git
   git branch -M main
   git push -u origin main
   ```

2. **Import to Vercel**
   - Go to [vercel.com/dashboard](https://vercel.com/dashboard)
   - Click "Add New..." → "Project"
   - Import your GitHub repository
   - Vercel will auto-detect settings
   - Click "Deploy"
   - Done! Your site will be live in seconds

3. **Your Site Will Be Live At**
   ```
   https://team-piratez-racing.vercel.app
   ```

### Method 2: Deploy via Vercel CLI (For Advanced Users)

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**
   ```bash
   vercel login
   ```

3. **Deploy**
   ```bash
   cd "d:\Website Piratez"
   vercel
   ```

4. **Follow the prompts:**
   - Set up and deploy? Yes
   - Which scope? Select your account
   - Link to existing project? No
   - What's your project's name? team-piratez-racing
   - In which directory is your code located? ./
   - Want to override settings? No

5. **Deploy to Production**
   ```bash
   vercel --prod
   ```

## Custom Domain (Optional)

1. Go to your project settings on Vercel Dashboard
2. Navigate to "Domains"
3. Add your custom domain (e.g., `www.teampiratez.racing`)
4. Follow DNS configuration instructions
5. Vercel will automatically provision SSL certificate

## Environment Setup

This is a static HTML/CSS/JS website, so no environment variables are required. However, if you add backend functionality later:

1. Go to Project Settings → Environment Variables
2. Add your variables
3. Redeploy

## Continuous Deployment

Once connected to GitHub, Vercel will automatically:
- Deploy every push to `main` branch to production
- Create preview deployments for pull requests
- Run build checks before deployment

## Quick Commands Reference

```bash
# Deploy to preview
vercel

# Deploy to production
vercel --prod

# List deployments
vercel ls

# View deployment logs
vercel logs

# Remove deployment
vercel rm [deployment-url]
```

## Troubleshooting

### Issue: "Command not found: vercel"
**Solution**: Install Vercel CLI globally
```bash
npm install -g vercel
```

### Issue: Fonts not loading
**Solution**: Fonts are loaded from Google Fonts CDN. Check your internet connection.

### Issue: Images not displaying
**Solution**: Ensure all image paths are correct and files are committed to Git.

### Issue: 404 errors
**Solution**: Vercel serves `index.html` by default. Navigation should work correctly.

## Performance Tips

Your website is already optimized with:
- ✅ Lazy loading images
- ✅ Intersection observers for animations
- ✅ Minified CSS (can be further optimized)
- ✅ CDN delivery via Vercel Edge Network

For even better performance:
1. Enable Vercel Analytics in project settings
2. Consider image optimization with Vercel's Image Optimization
3. Add a `robots.txt` and `sitemap.xml` for better SEO

## Support

- Vercel Documentation: https://vercel.com/docs
- Vercel Support: https://vercel.com/support
- Team Piratez: contact@teampiratez.racing

---

**Ready to Deploy?** Just run `vercel` in your project directory! 🚀

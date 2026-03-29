# Family Food Plan - Vercel Deployment Guide

## Quick Deploy Options

### Option 1: Deploy with Vercel CLI (Recommended)

```bash
# Install Vercel CLI (if not already installed)
npm install -g vercel

# Login to Vercel
vercel login

# Deploy to Vercel
vercel

# For production deployment
vercel --prod
```

### Option 2: Connect GitHub Repository to Vercel Dashboard

1. Go to [vercel.com](https://vercel.com)
2. Sign in with your GitHub account
3. Click **Add New...** → **Project**
4. Select your `family_food_plan` repository
5. Framework preset: **Other** (or leave blank)
6. Click **Deploy**

### Option 3: Manual Deploy via Dashboard

1. Go to [vercel.com/new](https://vercel.com/new)
2. Upload your project folder
3. Configure:
   - **Framework**: Other
   - **Output Directory**: (leave blank)
4. Click **Deploy**

---

## Current Project Structure

```
family_food_plan/
├── index.html              (Home page - entry point)
├── home_page.html          (Duplicate of index.html)
├── dad_diet.html           (Dad's 7-day diet plan)
├── mumma_diet.html         (Mumma's 7-day diet plan)
├── image.png               (Family circular image)
├── vercel.json             (Vercel routing config)
└── README.md               (This file)
```

---

## Deployment Tips

✅ **Your project is already Vercel-ready!**

- `index.html` is set as the default home page
- `vercel.json` handles clean URL routing
- All image assets are local and included
- No build step required (static site)

---

## After Deployment

Once deployed, your site will be available at:
- **Home**: `https://your-project.vercel.app/`
- **Dad Plan**: `https://your-project.vercel.app/dad` (or `/dad_diet.html`)
- **Mumma Plan**: `https://your-project.vercel.app/mumma` (or `/mumma_diet.html`)

---

## Environment & Requirements

- **Node.js**: Not required (static HTML)
- **Build Command**: None
- **Install Command**: None
- **Output Directory**: `.` (current directory)

---

## Push Updates to Vercel

After making changes locally:

```bash
# Commit changes
git add .
git commit -m "Update diet plans"

# Push to GitHub
git push origin main

# Vercel will auto-deploy from GitHub (if connected)
# OR manually deploy again with:
vercel --prod
```

---

## Support & Troubleshooting

- **Images not loading?** Verify `image.png` is in the root directory.
- **Routes not working?** Check that `vercel.json` is present and valid.
- **Slow deployment?** Clear Vercel cache: `vercel env pull` then `vercel --prod`.

Enjoy your live diet plan app! 🌿

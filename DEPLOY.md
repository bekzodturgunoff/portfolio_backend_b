# Backend Deployment Guide

## Quick Deploy to Vercel

### Step 1: Deploy the Backend

```bash
cd /Users/bekzod/Documents/code/portfolio/modern_portfolio/back_end
vercel
```

**Answer the prompts:**
- Set up and deploy? → **Y**
- Which scope? → **Select your account**
- Link to existing project? → **N**
- Project name? → **portfolio-backend** (or any name you like)
- In which directory is your code located? → **.**
- Want to override the settings? → **N**

This will give you a URL like: `https://portfolio-backend-xxx.vercel.app`

### Step 2: Add Environment Variables

```bash
vercel env add RESEND_API_KEY production
```
When prompted, paste: `re_J1wvcaYc_KP6rh38wZ9LY8nmWWMNo8G4k`

```bash
vercel env add ALLOWED_ORIGINS production
```
When prompted, paste: `https://ptbt.vercel.app`

### Step 3: Deploy to Production

```bash
vercel --prod
```

**Copy the production URL** you get (it will look like: `https://portfolio-backend.vercel.app`)

### Step 4: Update Frontend

Go to your frontend Vercel project dashboard at: https://vercel.com/dashboard

1. Select the **ptbt** project
2. Go to **Settings** → **Environment Variables**
3. Add new variable:
   - **Name**: `PUBLIC_API_BASE`
   - **Value**: `https://portfolio-backend.vercel.app` (paste your backend URL here)
   - **Environment**: Production, Preview, Development (select all)
4. Click **Save**
5. Go to **Deployments** tab
6. Click **...** on the latest deployment → **Redeploy**

---

## That's it! 🎉

Your contact form will now work on your live site at https://ptbt.vercel.app

### Testing

Visit https://ptbt.vercel.app and try submitting the contact form. You should receive an email at bekzodturgunoff@gmail.com

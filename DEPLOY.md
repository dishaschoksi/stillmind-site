# Still Mind — Deploy to Vercel

## Before you deploy: 2 things to update in index.html

Open `index.html` and find + replace these two placeholders:

1. `YOUR_PIXEL_ID` → your Meta Pixel ID (from Meta Business Suite → Events Manager)
2. `YOUR_STRIPE_CHECKOUT_LINK` → your Stripe payment link (from Stripe Dashboard → Payment Links)

---

## Step 1: Create a GitHub account (if you don't have one)
Go to https://github.com and sign up. Free account is fine.

---

## Step 2: Create a new GitHub repository

1. Click the **+** icon (top right) → **New repository**
2. Name it: `stillmind-site`
3. Set to **Public**
4. Do NOT check "Add a README file"
5. Click **Create repository**
6. Copy the repository URL — it will look like:
   `https://github.com/YOUR_USERNAME/stillmind-site.git`

---

## Step 3: Open Terminal (Mac) or Command Prompt (Windows)

On Mac: Press `Cmd + Space`, type "Terminal", press Enter.

Navigate to the stillmind-site folder. Replace the path below with wherever you saved the folder:

```bash
cd /path/to/stillmind-site
```

For example, if it's in your Downloads:
```bash
cd ~/Downloads/stillmind-site
```

---

## Step 4: Push to GitHub

Run these commands one at a time (paste each line, press Enter):

```bash
git init
git add .
git commit -m "Initial commit: Still Mind landing page"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/stillmind-site.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

When prompted, enter your GitHub username and password (or personal access token).

---

## Step 5: Deploy on Vercel

1. Go to https://vercel.com and sign up with your GitHub account
2. Click **Add New** → **Project**
3. Click **Import Git Repository**
4. Find `stillmind-site` and click **Import**
5. On the configuration screen:
   - Framework Preset: **Other**
   - Build Command: leave blank
   - Output Directory: leave blank
6. Click **Deploy**

Vercel will build and deploy in ~15 seconds.

---

## Step 6: Your site is live

You'll get a URL like: `https://stillmind-site.vercel.app`

That is your landing page URL. Use this in your Meta ad campaigns.

---

## Step 7: Add a custom domain (optional but recommended)

In Vercel Dashboard → your project → **Settings** → **Domains**:
- Add a domain like `stillmind.com` or `getmindclarity.com`
- Vercel gives you DNS instructions to follow with your domain registrar (GoDaddy, Namecheap, etc.)
- Takes 10-30 minutes to go live

---

## After deployment: update your ads

Once live, go back to Meta Ads Manager and update the destination URL in your ads to your new Vercel URL.

---

## To update the page in future

Whenever you edit `index.html`, run:

```bash
git add .
git commit -m "Update landing page"
git push
```

Vercel auto-deploys on every push. Your site will update in ~15 seconds.

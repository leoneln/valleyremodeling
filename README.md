# Valley Remodeling LLC — Website

**Live URL:** [https://valleyremodeling.llc](https://valleyremodeling.llc)

A professional single-page website for Valley Remodeling LLC, serving the Salt Lake Valley, Utah. Built with pure HTML, CSS, and vanilla JavaScript — no build tools or frameworks required.

---

## 📁 Files in This Repository

| File | Description |
|---|---|
| `index.html` | The complete website (all HTML, CSS, and JS in one file) |
| `CNAME` | Custom domain file for GitHub Pages (create this — see below) |
| `README.md` | This file |

---

## 🚀 Deploying to GitHub Pages (Step-by-Step)

### Step 1 — Create a GitHub Account
1. Go to [https://github.com](https://github.com)
2. Click **Sign up** and follow the prompts
3. Verify your email address

---

### Step 2 — Create a New Repository
1. Click the **+** icon in the top-right → **New repository**
2. Name it exactly: `valleyremodeling.llc`
   *(or any name you like — the domain will be set separately)*
3. Set it to **Public**
4. Leave "Initialize with README" **unchecked**
5. Click **Create repository**

---

### Step 3 — Upload Your Files
**Option A — Upload via GitHub's web interface (easiest):**
1. Open your new repository page
2. Click **uploading an existing file** (or drag and drop)
3. Upload `index.html` and (optionally) `CNAME`
4. Scroll down → write a commit message like `Initial website upload`
5. Click **Commit changes**

**Option B — Using Git on your computer:**
```bash
git init
git add .
git commit -m "Initial website upload"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/valleyremodeling.llc.git
git push -u origin main
```

---

### Step 4 — Enable GitHub Pages
1. In your repository, click the **Settings** tab (gear icon)
2. In the left sidebar, click **Pages**
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click **Save**
5. GitHub will show: *"Your site is published at https://YOUR_USERNAME.github.io/valleyremodeling.llc/"*

Your site will be live within 1–3 minutes at that URL.

---

### Step 5 — Connect Your Custom Domain (valleyremodeling.llc)

#### 5a. Create the CNAME file
Create a plain text file named exactly `CNAME` (no extension) with this single line inside:
```
valleyremodeling.llc
```
Upload it to the root of your GitHub repository (same folder as `index.html`).

#### 5b. Configure DNS at your domain registrar
Log into wherever you purchased `valleyremodeling.llc` and add these DNS records:

**A Records** — point the apex domain to GitHub's servers:
| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**CNAME Record** — for the `www` subdomain:
| Type | Name | Value |
|---|---|---|
| CNAME | www | YOUR_USERNAME.github.io |

> DNS changes can take anywhere from a few minutes to 48 hours to fully propagate worldwide.

#### 5c. Enable HTTPS (free)
1. Go back to **Settings → Pages** in your GitHub repository
2. Once the custom domain is verified, check **Enforce HTTPS**
3. Your site will now be securely accessible at `https://valleyremodeling.llc` ✅

---

## ✏️ Customizing Your Website

### Update Phone Number
Find and replace `(801) 555-0100` and `+18015550100` throughout `index.html` with the real phone number.

> Search for `555-0100` to find all instances quickly.

### Update Email Address
Find and replace `info@valleyremodeling.llc` with the real contact email address.

### Update Business Hours
Search for `7:00 AM – 6:00 PM` and change to the actual business hours.

### Update the "Trusted Since" Year
The hero badge reads "Trusted Since 2003" — update this to match the actual founding year.

### Update Copyright Year
Search for `© 2025` and update as needed each year.

---

## 📧 Setting Up the Contact Form (Recommended)

The current form uses a basic `mailto:` action, which opens the user's email app. For a more professional, reliable experience that sends form submissions directly to your inbox, use **Formspree** (free tier available):

1. Go to [https://formspree.io](https://formspree.io) and sign up for free
2. Click **New Form** and name it something like "Valley Remodeling Estimates"
3. Copy your unique form endpoint URL (looks like `https://formspree.io/f/XXXXXXXX`)
4. In `index.html`, find this comment:
   ```html
   <!-- TO ENABLE FORM EMAIL DELIVERY: -->
   ```
5. Change the `<form>` tag's `action` attribute from:
   ```html
   action="mailto:info@valleyremodeling.llc" method="post" enctype="text/plain"
   ```
   To:
   ```html
   action="https://formspree.io/f/XXXXXXXX" method="POST"
   ```
6. Save and re-upload `index.html` to GitHub

Now every form submission will be emailed directly to you — no email app required from the visitor.

---

## 🖼️ Replacing Stock Images with Real Photos

The website uses [Unsplash](https://unsplash.com) stock images. To replace them with real photos of completed projects:

1. Upload your photos somewhere accessible (Google Drive public link, Imgur, your own hosting)
2. In `index.html`, find the `<img>` tags with `images.unsplash.com` URLs
3. Replace the `src="..."` URL with your image URL or filename
4. For local images: create an `images/` folder in your repository and upload photos there, then reference them as `src="images/your-photo.jpg"`

**Recommended image dimensions:**
- Service cards: 600 × 420 px
- Gallery items: 700 × 560 px
- About section main image: 820 × 600 px

---

## 📱 Features

- ✅ Fully responsive — works on mobile, tablet, and desktop
- ✅ Smooth scroll animations on all sections
- ✅ Auto-advancing testimonial carousel with navigation
- ✅ Sticky navigation with scroll effect
- ✅ Mobile hamburger menu
- ✅ Interactive contact / estimate request form
- ✅ Google Maps embed showing the Salt Lake Valley service area
- ✅ Prominent phone number CTAs with `tel:` links (tap-to-call on mobile)
- ✅ SEO meta tags and Open Graph tags included
- ✅ Lazy-loading images for fast performance
- ✅ No external dependencies — no npm, no build step required

---

## 🛠️ Making Future Edits

After any changes to `index.html`:
1. Go to your GitHub repository
2. Click on `index.html`
3. Click the **pencil ✏️ icon** to edit in browser, OR upload the new file (it will replace the old one)
4. Commit the changes — GitHub Pages will auto-redeploy within 1–2 minutes

---

## 📞 Support

For questions about this website, contact the developer or refer to:
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Formspree Documentation](https://help.formspree.io)
- [Unsplash (free stock photos)](https://unsplash.com)

---

*Built for Valley Remodeling LLC — Salt Lake Valley, Utah*

# Gullakaari NGO Website

Static website for Gullakaari Foundation — an NGO reviving India's endangered handicraft art forms.

**Live URL:** https://gullakaari.techpose.in

## Pages

| File | Description |
|------|-------------|
| `index.html` | Home page — intro, mission, key highlights, stats |
| `about.html` | About Us / Our Story — journey, vision, team |
| `programs.html` | Programs / Impact — art forms, impact stories |
| `donate.html` | Donation Information — bank details, UPI |
| `contact.html` | Contact — details + Google Form embed |

## Deployment: GitHub Pages

### Step 1 — Create GitHub Repository
1. Go to https://github.com/new
2. Name it `gullakaari` (or any name you prefer)
3. Set to **Public** (required for free GitHub Pages)
4. Click **Create repository**

### Step 2 — Push the code
```bash
cd gullakaari/
git init
git add .
git commit -m "Initial website launch"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/gullakaari.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. The workflow at `.github/workflows/deploy.yml` will auto-deploy

### Step 4 — Custom Subdomain (gullakaari.techpose.in)
The `CNAME` file already contains `gullakaari.techpose.in`.

**In your domain DNS panel (for techpose.in):**
Add a CNAME record:
```
Type:  CNAME
Host:  gullakaari
Value: YOUR_USERNAME.github.io
TTL:   3600
```

After DNS propagates (up to 24h), your site will be live at https://gullakaari.techpose.in

### Step 5 — Force HTTPS
In GitHub repo → Settings → Pages → check **Enforce HTTPS**

---

## Customization Checklist

- [ ] Replace `contact@gullakaari.org` with actual email
- [ ] Add real bank account details in `donate.html`
- [ ] Add real UPI ID in `donate.html`  
- [ ] Replace Google Form embed URL in `contact.html`:
  - Open your Google Form → Send → Embed (`<>`) → copy the iframe `src` URL
  - Paste it in `contact.html` replacing `YOUR_GOOGLE_FORM_EMBED_URL_HERE`
- [ ] Replace placeholder images with actual Gullakaari photos
- [ ] Update team details in `about.html`
- [ ] Update `sitemap.xml` dates when you make changes

## File Structure

```
gullakaari/
├── index.html          # Home page
├── about.html          # About Us
├── programs.html       # Programs & Impact
├── donate.html         # Donation page
├── contact.html        # Contact + Google Form
├── css/
│   └── style.css       # All styles
├── js/
│   └── main.js         # Navigation logic
├── CNAME               # Custom domain config
├── robots.txt          # SEO crawler rules
├── sitemap.xml         # SEO sitemap
└── .github/
    └── workflows/
        └── deploy.yml  # Auto-deploy to GitHub Pages
```

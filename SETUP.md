# Ultra Normal — Website Setup Guide

## Your files
- `index.html` — Home page
- `about.html` — About page
- `blog.html` — Blog page
- `work-with-me.html` — Physio services + enquiry form
- `css/style.css` — All styles
- `js/main.js` — All interactivity

---

## Getting live on GitHub Pages (free hosting)

### Step 1 — Create a GitHub account
Go to https://github.com and sign up for a free account.
Choose a username — ideally `ultranormal` or similar.

### Step 2 — Create a new repository
1. Click the **+** icon (top right) → **New repository**
2. Name it: `ultra-normal`
3. Set it to **Public**
4. Click **Create repository**

### Step 3 — Upload your files
1. Click **uploading an existing file** (on the new repo page)
2. Drag ALL files and folders from this zip into the upload area
   - Make sure the `css/` and `js/` folders upload with their contents
3. Click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to your repo → **Settings** tab
2. Scroll to **Pages** in the left sidebar
3. Under **Source**, select **main** branch, **/ (root)** folder
4. Click **Save**

### Step 5 — Your site is live!
GitHub will give you a URL like:
`https://yourusername.github.io/ultra-normal`

It takes 1–2 minutes to go live. Share this link in your Instagram bio!

---

## Things to personalise before going live

### Must-do
- [ ] Replace "YOUR PHOTO HERE" placeholders with real photos on About page
- [ ] Update Instagram/YouTube links with your actual handles
- [ ] Replace `[Your qualifications here]` on the About page
- [ ] Update the stats on the Home page (weeks training, etc.)

### Form setup (to receive enquiries)
The enquiry form currently shows a success message but doesn't email you.
To receive emails from the form:

**Option A — Formspree (free, easiest)**
1. Go to https://formspree.io and create a free account
2. Create a new form, copy your form endpoint URL
3. In `work-with-me.html`, find `<form id="enquiryForm">`
4. Add: `action="https://formspree.io/f/YOUR_ID" method="POST"`
5. In `js/main.js`, remove the `e.preventDefault()` line in the enquiryForm handler

**Option B — Keep as-is**
The form shows a thank-you message. You can direct people to DM you on Instagram instead for now — totally fine for launch.

### When you buy a domain
1. Buy `ultranormal.com.au` from Namecheap or Google Domains
2. In GitHub repo Settings → Pages → Custom domain, enter your domain
3. Follow GitHub's DNS instructions (they walk you through it)
4. Takes 24–48 hours to propagate

---

## Adding blog posts
Each blog post is a new HTML file. Copy this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>POST TITLE — Ultra Normal</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <!-- Copy nav from any other page -->
  
  <div class="page-hero">
    <div class="container">
      <span class="eyebrow eyebrow--light">CATEGORY · WEEK X</span>
      <h1 class="page-hero__title">POST TITLE</h1>
      <p class="page-hero__sub">Short description.</p>
    </div>
  </div>

  <section class="section">
    <div class="container" style="max-width:720px;">
      <p>Your content here...</p>
    </div>
  </section>

  <!-- Copy footer from any other page -->
  <script src="js/main.js"></script>
</body>
</html>
```

Save as e.g. `posts/week-1-ai-coach.html` and link to it from `blog.html`.

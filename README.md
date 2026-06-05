# tylerallenmcdonald.com

Personal website for Tyler Allen McDonald — BI analyst, photographer, surfer.

Built with plain HTML and CSS. Hosted on GitHub Pages.

---

## File structure

```
/
├── index.html              ← Home page
├── css/
│   └── style.css           ← All styles (colors, fonts, layout)
├── pages/
│   ├── about.html          ← About Me
│   ├── work.html           ← Work & Projects
│   ├── resume.html         ← Résumé
│   └── bookmarks.html      ← Bookmarks
├── photos/                 ← Put your images here (create this folder)
│   └── (your photos)
├── tyler-allen-mcdonald-resume.pdf   ← Drop your PDF resume here
└── README.md
```

---

## Deploying to GitHub Pages

1. Upload all files to the `tylerallenmcdonald.github.io` repo
2. Go to **Settings → Pages** → set source to main branch, / (root)
3. Add `tylerallenmcdonald.com` as the custom domain
4. Add a `CNAME` file at the root containing just: `tylerallenmcdonald.com`
5. Update DNS at your domain registrar:
   - 4 A records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - CNAME record: `www` → `tylerallenmcdonald.github.io`

---

## How to make common edits

### Change a color
Open `css/style.css` and find the **Variables** section near the top.
Change the hex value next to the variable you want:
```css
--blue:   #2c5f8a;   /* change this hex to any color */
--orange: #c97a4a;   /* change this for the accent color */
```

### Change font size
In `css/style.css`, find the `html` rule:
```css
html { font-size: 17px; }
```
Increase or decrease this number. Everything scales with it.

### Add a project (work.html)
Copy the project card block and fill in your details:
```html
<div class="project-card">
  <div>
    <div class="project-meta">
      <span class="tag">SQL</span>
      <span class="tag">Tableau</span>
    </div>
    <h3>Your project title</h3>
    <p>Description of what you built and why.</p>
    <a class="project-link" href="https://github.com/tylerallenmcdonald/your-repo" target="_blank">
      View on GitHub →
    </a>
  </div>
  <span class="project-year">2025</span>
</div>
```

### Add a photo (index.html or about.html)
1. Create a `photos/` folder at the project root
2. Drop your image file in there (e.g. `headshot.jpg`)
3. In `index.html`, replace the `<div class="photo-placeholder">` block with:
```html
<img src="photos/headshot.jpg" alt="Tyler Allen McDonald" />
```
4. In `about.html`, replace `<div class="photo-frame">Photo</div>` with:
```html
<img src="../photos/your-photo.jpg" alt="Description of photo" />
```
(Note the `../` — needed because about.html is inside the `pages/` folder)

### Add a bookmark (bookmarks.html)
Copy this block and paste it at the top of the list (newest first):
```html
<div class="bookmark-item" data-type="article">
  <span class="bookmark-type article">Article</span>
  <div>
    <a class="bookmark-title" href="https://your-link.com" target="_blank" rel="noopener">
      Title of the thing
    </a>
    <p class="bookmark-source">Source name</p>
    <p class="bookmark-note">Optional note about why it's interesting.</p>
    <p class="bookmark-date">June 2026</p>
  </div>
</div>
```
Change `article` to `music`, `video`, `art`, or `other` in both the
`data-type` attribute and the `bookmark-type` class.

### Add a job to the résumé (resume.html)
Copy this block and paste it at the top of the Experience section:
```html
<div class="resume-entry">
  <div>
    <h3>Job Title</h3>
    <p class="company">Company Name · City, ST</p>
    <ul>
      <li>Accomplishment or responsibility</li>
      <li>Another one</li>
    </ul>
  </div>
  <span class="dates">20XX – 20XX</span>
</div>
```

---

## Things still to fill in

- [ ] Bio text in each section of `about.html`
- [ ] Real job titles, companies, and dates in `resume.html`
- [ ] Actual skills in the skills grid in `resume.html`
- [ ] Your email on `resume.html` (already on home and about)
- [ ] First real project in `work.html`
- [ ] Your headshot in `index.html`
- [ ] Travel photos in `about.html`
- [ ] PDF résumé → `tyler-allen-mcdonald-resume.pdf` at root
- [ ] Real bookmarks replacing the example ones in `bookmarks.html`
- [ ] LinkedIn URL (confirm it's `tylerallenmcdonald`)

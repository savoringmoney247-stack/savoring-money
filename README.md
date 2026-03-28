# Savoring Money — The Global Polymath Academy
### GitHub Pages Site

A complete financial education platform and resource hub hosted on GitHub Pages.

---

## 📁 File Structure

```
/  (root)
├── index.html                        ← Main Hub (homepage)
├── Savoring_Money_Website.htm        ← Main website
├── Savoring_Money_Careers.htm        ← Careers portal
├── SavoringMoney_ATS.html            ← ATS / People Ops (internal)
├── __SAT_Math_Mastery_Tracker.html   ← SAT Math Tracker
├── Invest_Universe.html              ← Investment Universe
├── README.md                         ← This file
└── worksheets/
    ├── index.html                    ← Worksheets Hub (EDITABLE)
    └── files/                        ← Place your worksheet files here
        ├── *.pdf
        ├── *.docx
        ├── *.xlsx
        ├── *.png / *.jpg
        └── *.html
```

---

## 🚀 How to Host on GitHub Pages

### Step 1 — Create a GitHub Repository
1. Go to [github.com](https://github.com) and sign in
2. Click **"New repository"** (top right → `+`)
3. Name it: `savoring-money` (or anything you prefer)
4. Set visibility to **Public** (required for free GitHub Pages)
5. Click **"Create repository"**

### Step 2 — Upload All Files
**Option A — GitHub Web Interface (easiest):**
1. Open your new repository
2. Click **"uploading an existing file"** or drag-and-drop
3. Upload ALL files maintaining the folder structure:
   - Upload root files first
   - Then create `worksheets/` folder and upload `worksheets/index.html`
   - Create `worksheets/files/` and upload your worksheet files there
4. Click **"Commit changes"**

**Option B — Git CLI:**
```bash
git init
git add .
git commit -m "Initial deploy: Savoring Money Hub"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/savoring-money.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. Go to your repository → **Settings**
2. Scroll to **"Pages"** in the left sidebar
3. Under **"Branch"**, select `main` and folder `/` (root)
4. Click **Save**
5. Wait 1–2 minutes → your site goes live at:
   ```
   https://YOUR_USERNAME.github.io/savoring-money/
   ```

---

## ✏️ How to Add Worksheets

Open `worksheets/index.html` in any text editor (VS Code, Notepad, etc.).

Find the comment block:
```html
<!-- 👆 ADD YOUR NEW WORKSHEETS ABOVE THIS LINE -->
```

Copy any existing `<a class="ws-card ...">` block above it. Then:

| File Type | Card Class | Badge Class | `data-type` |
|-----------|-----------|-------------|-------------|
| PDF | `c-pdf` | `badge-pdf` | `pdf` |
| Word Doc | `c-doc` | `badge-doc` | `doc` |
| HTML Tool | `c-html` | `badge-html` | `html` |
| Image | `c-img` | `badge-img` | `img` |
| Spreadsheet | `c-xlsx` | `badge-xlsx` | `xlsx` |
| External URL | `c-link` | `badge-link` | `link` |

**Example — adding a PDF:**
```html
<a href="files/my-worksheet.pdf" class="ws-card c-pdf" data-type="pdf">
  <div class="ws-type-badge badge-pdf">PDF</div>
  <div class="ws-info">
    <div class="ws-title">My Worksheet Title</div>
    <div class="ws-desc">Short description of what this worksheet covers</div>
  </div>
  <div class="ws-meta">
    <span class="ws-tag">Category</span>
    <span class="ws-arrow">↗</span>
  </div>
</a>
```

Place the actual file in `worksheets/files/my-worksheet.pdf`, commit and push.

---

## 🔄 Updating Files

Every time you edit any file:
1. Make your changes locally
2. Run:
   ```bash
   git add .
   git commit -m "Update: describe what changed"
   git push
   ```
3. GitHub Pages auto-updates within ~30 seconds.

Or use the GitHub web editor: open any file → pencil icon → edit → commit.

---

## 🌐 Custom Domain (Optional)

To use `www.savoringmoney.com` instead of `github.io`:
1. Settings → Pages → Custom domain → enter your domain
2. At your domain registrar, add a CNAME record pointing to `YOUR_USERNAME.github.io`
3. GitHub will auto-issue an SSL certificate

---

*Built with ❤️ · The Global Polymath Academy*

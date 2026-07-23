# fabiosalvador.com — setup guide

This folder is a complete, GitHub Pages-ready website. Every image is currently a
labelled grey placeholder — the label tells you the exact size to export your real
image at. Replace the file, keep the same name, and the site updates itself.

## 1. Publish on GitHub Pages

1. Create a new repository on github.com (e.g. `fabiosalvador.com`), public.
2. Upload the **contents** of this folder (index.html, CNAME, images/) to the repo root
   — drag-and-drop works on the GitHub website ("Add file → Upload files").
3. Repo → Settings → Pages → Source: "Deploy from a branch" → Branch: `main`, folder `/ (root)` → Save.
4. In your domain registrar, point `fabiosalvador.com`:
   - Four A records: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - CNAME record for `www` → `YOUR-GITHUB-USERNAME.github.io`
5. Back in Settings → Pages, enter `fabiosalvador.com` as the custom domain and tick
   "Enforce HTTPS" once the certificate is issued (can take up to an hour).

The `CNAME` file in this folder is already set to `fabiosalvador.com` — don't delete it.

## 2. Your logo

Export from Illustrator/vector source as **SVG** (File → Export → SVG, text converted
to outlines). Name it `logo.svg`, drop it into `images/`, then in `index.html` find the
comment `LOGO — TEMPORARY TEXT PLACEHOLDER` and replace the placeholder markup with:

```html
<img src="images/logo.svg" alt="Fábio Salvador" style="width:100%;display:block;">
```

Also export a PNG at ~1600 px wide on transparent background for social sharing
if you want an `og:image` later.

## 3. CV download (Google Drive)

1. Upload your CV PDF to Google Drive → Share → "Anyone with the link".
2. Copy the FILE_ID from the share URL: `https://drive.google.com/file/d/FILE_ID/view`
3. In `index.html`, find `CV_DOWNLOAD_URL` and replace `REPLACE_WITH_FILE_ID`.
4. Export page 1 of the PDF as a JPG and save it as `images/cv/cv-preview.jpg`.

## 4. New project copy

The three new projects (McLaren Configurator, Valkyrie Industries, PurePods) and the
five hobby slides have `[PLACEHOLDER — …]` text in the `PROJECTS` and `HOBBIES` arrays
in `index.html`. Search for `PLACEHOLDER` and replace each with your own copy.
Character limits are noted in the comments (navDesc 45 / cardText 100 /
aboutProject 550 / moreInfo 350).

## 5. Social links

In `index.html`, search for `YOUR-LINKEDIN-HANDLE` and `YOUR-BEHANCE-HANDLE` and
replace with your real profile URLs.

## 6. Images from your existing site

The 8 carried-over projects use the same folder names and file names as your
makersdepartment.com repo (`images/projects/<slug>/thumb.jpg`, `card.jpg`, `hero.jpg`,
plus `images/slideshow/` and `images/about/`). You can copy those folders straight
across from the makersdepartment repo and they'll drop into place.

For the new sections, export at the size written on each placeholder:

| File | Size |
|---|---|
| images/projects/&lt;slug&gt;/thumb.jpg | 300 × 200 |
| images/projects/&lt;slug&gt;/card.jpg | 1200 × 800 |
| images/projects/&lt;slug&gt;/hero.jpg | 1800 × 1200 |
| images/slideshow/slide-01…10.jpg | 1800 × 1200 |
| images/hobbies/hobby-01…05.jpg | 1800 × 1200 |
| images/cv/cv-preview.jpg | 840 × 1188 (A4 ratio) |

## 7. Favicon (optional)

Add `favicon.ico` to the root when ready — the HTML already references it.

# GitHub Pages deployment

Repository: https://github.com/Leafyve/azoom-car-rental
Pages target: https://leafyve.github.io/azoom-car-rental/

Configuration: deploy from `main`, root directory `/`, with `.nojekyll` to serve the existing static HTML/CSS/JavaScript. All runtime images and fonts are local and use relative URLs. No custom build workflow is needed.

Status: **Successfully deployed and verified on 29 October 2026.** The GitHub Pages build completed successfully for `90dfcd37d999f7f5c22e8afc473ce0d0e0739f20`. The actual public URL returned HTTP 200 and passed 22 browser checks. See `LIVE_VERIFICATION.md` for evidence and limits.

## Push future updates

Open PowerShell in the website directory:

```powershell
Set-Location -LiteralPath 'C:\Users\En Le\Downloads\ISIT207 Web\ISIT207_Assignment2_Complete_Package\AZoom_Car_Rental'
git status --short
git pull --ff-only origin main
# Edit the website, then review the exact changes:
git diff
# Stage only the files you intentionally changed, for example:
git add -- index.html style.css script.js
# If you changed an image, stage that exact asset and its credits too.
git diff --cached --stat
git diff --cached
git commit -m "Update AZoom website content"
git push origin main
```

If `git pull --ff-only` reports conflicting or divergent work, stop and review before proceeding. Do not force-push. After pushing, wait for **Actions > pages build and deployment** to complete, then open the public site and refresh to test the changed content.

The `.gitignore` excludes the university PDF report, document archives, local screenshots, video, test profiles, temporary files, credentials and legacy SVG illustrations. Check staged filenames before each commit. Keep student IDs and real customer information outside this public repository.

## Local preview

```powershell
py -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000 . Demo bookings are browser-local and do not transfer between local and public origins.

Official documentation: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

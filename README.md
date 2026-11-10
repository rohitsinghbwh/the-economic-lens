# The Economic Lens

A responsive, static-first economics publication starter website. It includes editorial landing sections for articles, columns, research, an About page, and an interactive India macro dashboard.

## Run locally

Open `index.html` in a browser. For best results, serve the folder through a local static server (for example, `python -m http.server 8000`) because browsers may restrict API requests from `file://` pages.

## Included

- Responsive editorial layout
- Sections for articles, columns, research and about
- India macro dashboard using the World Bank Indicators API
- Visible fallback values if the API is unavailable (marked as illustrative)
- Pages CMS configuration in `.pages.yml` for a simple GitHub-based editing workflow

## Important data note

The dashboard requests annual observations from the World Bank API. These are not real-time market data. If the API is unavailable, the page shows illustrative fallback values and labels them accordingly. Replace or remove these fallback values before using screenshots or values in research or publication.

## Publish for free

1. Create a GitHub account at https://github.com/ and create a new **public** repository named `the-economic-lens`.
2. Upload the contents of this folder to the repository root (not the folder itself). Commit to the `main` branch.
3. Create a free Cloudflare account at https://dash.cloudflare.com/.
4. In Cloudflare, open **Workers & Pages → Create → Pages → Connect to Git**. Select the GitHub repository.
5. For a plain static site, use no build command and set the build output directory to `/` (or `.` if the interface requests a relative directory). Deploy.
6. Cloudflare will provide a free `*.pages.dev` address. You can later attach a custom domain, but domain registration generally costs money.
7. To edit posts with a visual editor, visit https://app.pagescms.org/, sign in with GitHub, install/authorize the Pages CMS GitHub App for this repository, and open the repository. The `.pages.yml` file defines the editable article collection. Save changes in Pages CMS; the Git commit triggers a Cloudflare redeploy.

Cloudflare's current Pages Free documentation lists 500 builds per month and up to 20,000 files per site; check current plan limits before relying on them: https://developers.cloudflare.com/pages/platform/limits/.

## First edits to make

- Replace the sample editorial content with your own writing and properly sourced references.
- Change the About copy and contact email (`hello@youremail.example`) to your preferred public contact address.
- Review `content/articles.json` and `.pages.yml` before first use of the CMS.
- Add a privacy policy and editorial/disclaimer page before collecting visitor information or publishing research.

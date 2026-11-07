# Plink Piano website

The public site for Plink Piano (iOS app): home, privacy policy and terms of use.
Static HTML and CSS, no build step, served by GitHub Pages from `main` at the root.

- `index.html`: the home page.
- `privacy.html`: the privacy policy. App Store Connect's privacy policy URL points here.
- `terms.html`: the terms of use. Subscriptions use Apple's standard EULA plus these terms.
- `guides/`: answer pages for search engines and AI assistants (GEO plan:
  /mnt/project-files/website/geo/plan.md). Each answers in its first lines, carries a
  "Last updated" date and Article JSON-LD, and goes into `sitemap.xml` and `llms.txt`.
- `style.css`: the app's colours (Theme.swift), light and dark.
- `sitemap.xml`, `llms.txt`: every page, with its last-changed date. Add new pages to both.
- `.github/workflows/indexnow.yml` and the `<key>.txt` file: tell Bing about the pages after
  every push to main (ChatGPT search draws on Bing).
- Every page has a canonical URL and a meta description. The home page has
  SoftwareApplication JSON-LD that matches its visible text; add `offers` and the App Store
  link once the app is live.

A custom domain (plinkpiano.com) can come later: add a `CNAME` file and set the DNS.

VoyaCue bilingual website package (VI/EN)

Deploy using GitHub repository Vincent102ct/voyacue-site (main), already connected to Cloudflare Pages.

1. Keep existing file paths. Upload/replace the following files with those in this ZIP:
   index.html, support.html, privacy.html, terms.html, styles.css.
2. Create folder en/ and upload its four HTML files:
   en/index.html, en/support.html, en/privacy.html, en/terms.html.
3. Keep existing assets/ images; bundled here in case you upload the entire site.
4. Commit to main. Cloudflare Pages Git integration should deploy automatically.
5. Test:
   https://voyacue-site.pages.dev/support.html (VI)
   https://voyacue-site.pages.dev/en/support.html (EN)
   https://voyacue-site.pages.dev/privacy.html (existing App Store URL, unchanged)
   https://voyacue-site.pages.dev/en/privacy.html (EN)
   https://voyacue-site.pages.dev/terms.html
   https://voyacue-site.pages.dev/en/terms.html
   https://voyacue-site.pages.dev/en/index.html
6. Switch VI / EN in header on desktop and mobile; check links and email.

Notes:
- Existing Vietnamese URLs remain unchanged for App Store Connect.
- This package translates current website content; it does not independently verify claims about MediaPipe SDK data collection. Resolve ongoing privacy audit before publishing a binding legal assertion.
- GitHub connected integration has read permission only from this session (403 when trying to write); upload manually to GitHub.

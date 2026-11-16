# VoyaCue Site — static Affiliate catalog patch

## Scope
Add **only** `affiliate/v1/catalog.json` to the root of the existing `Vincent102ct/voyacue-site` repository, branch `main` (Cloudflare Pages Git deployment).

Current source: `Vincent102ct/VoyaCue_Affiliate` `master`, `affiliate/v1/catalog.json`, checked 2026-11-16. The product and entire catalog remain `enabled: false`. This patch does not include the Affiliate Manager or any login/admin feature. It does not modify `index.html`, `privacy.html`, `support.html`, `terms.html`, `en/` or `assets/`.

## Deploy via GitHub Web UI
1. Go to https://github.com/Vincent102ct/voyacue-site (branch `main`).
2. Choose **Add file → Upload files**; drag the **`affiliate` folder** from this patch folder so GitHub preserves the full relative path `affiliate/v1/catalog.json`. Alternatively create `affiliate/v1/catalog.json` with **Add file → Create new file** and paste its contents.
3. Verify the changed file list contains **only** `affiliate/v1/catalog.json`.
4. Commit message: `chore(affiliate): add disabled static catalog to site`.
5. Allow the existing Cloudflare Pages Git integration to deploy.
6. Open `https://voyacue-site.pages.dev/affiliate/v1/catalog.json` and verify the response is JSON, `schemaVersion == 1`, `enabled == false`, and every product has `enabled == false`.
7. Verify website pages unchanged: `/`, `/privacy.html`, `/support.html`, `/terms.html`, `/en/`.

## Important
- This artifact has **not** been pushed to GitHub or deployed. The linked GitHub integration returned `403` on branch creation and file writing.
- Do **not** upload the local admin files or any secrets to this public repository.
- Keep the existing affiliate Worker for now. Do not delete it until iOS integration and any old clients have been checked.
- VoyaCue's Flutter endpoint migration is **not part of this patch**. App build 1.0.0 (9) must not be modified.
- The current JSON contains only a disabled Reuzel testing product with no pose links; it does not mean Affiliate is active.

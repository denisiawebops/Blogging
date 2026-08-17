# SEO indexing hotfix

Applied to this repository snapshot:

1. Rebuilt `sitemap.xml` so it contains only HTML files that actually exist in this repository, with the homepage at `/`.
2. Corrected the `employee-transportation.html` canonical URL.
3. Replaced internal links using the retired `employee-transportion.html` spelling.
4. Added Cloudflare Pages 301 redirects for renamed URLs. The permanently removed legacy URLs are intentionally not placed in the sitemap or internal links; Cloudflare Pages `_redirects` does not support 410 as a Pages redirect rule, so those retired paths should remain ordinary 404s unless a Worker/Rules-based 410 is intentionally deployed.

## Important production-source mismatch

The live site currently exposes additional pages that are not present in the uploaded repository snapshot, including several Google guide pages and the real-estate CRM article. Therefore this hotfix must be merged into the latest production/GitHub source rather than blindly replacing the current live repository with this snapshot.

## Google Search Console

After deployment:

- Submit/refresh `https://www.denisiawebops.org/sitemap.xml` in Search Console.
- Inspect representative URLs and run **Test live URL**.
- Request indexing for priority pages only.
- For removed URLs, do not request indexing; Google should process the 301 or 404 response.

Google does not guarantee immediate indexing; crawl/index timing remains algorithmic.

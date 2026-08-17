# Production indexing merge map

## URLs visible on current production but absent from the uploaded repository snapshot

These were found on the current live Denisia Webops site/content but are not present in the provided ZIP. Do **not** delete them when applying the sitemap hotfix to the real production repository.

- https://www.denisiawebops.org/google-ads-guide.html
- https://www.denisiawebops.org/google-analytics-guide.html
- https://www.denisiawebops.org/google-business-profile-2026-guide.html
- https://www.denisiawebops.org/google-products-hub.html
- https://www.denisiawebops.org/google-search-console-guide.html
- https://www.denisiawebops.org/google-tag-manager-guide.html
- https://www.denisiawebops.org/custom-crm-for-real-estate.html

The final production sitemap must include these only after confirming that each URL returns HTTP 200 and has a self-referencing canonical URL.

## Legacy URLs from the Search Console screenshot

### Renamed / fixed with 301
- /app.html -> /apps.html
- /employee-transportion.html -> /employee-transportation.html
- /ai-models.html -> /ai.html
- /omnifreq-water-imprinting-guide.html -> /omnifreq.html
- /caustics-studio.html -> /Caustics-studio.html
- /employee-commute-software-shuttle-apps.html -> /employee-commute-software-shuttle-app.html

### Permanently removed candidates
These paths are not present in the supplied repository snapshot and had no current search result when checked:
- /echo-restaurant-intelligence-system.html
- /functional-qr-menu-system.html
- /how-to-build-website-crm-erp-microsoft-pages-clean.html
- /qr-code-menu-generator.html
- /restaurant-customer-analytics.html
- /restaurant-qr-menu-ordering-system.html

For these, keep them out of the sitemap and remove internal links. If the pages are intentionally retired, ordinary 404 is acceptable on Cloudflare Pages; use a Worker/Rules-based 410 only if you deliberately want an explicit 410 implementation.

# Charleston walking guide — GitHub Pages package

Prepared for **ncmsec** and **forensiclawoffice.com**. This package is ready to publish; its presence on this computer does not mean GitHub or DNS has been configured.

The map contains 99 places, including **Church and Union Charleston (97)**, **Vintage Lounge (98)**, and **Cooper Coffee & Wine (99)**. The guide includes walking estimates, venue links, an event schedule, suggested days and walking loops. The site is responsive and needs no build service, database, API key or paid hosting plan.

## Publish

1. Sign in as ncmsec and open the existing **ncmsec/CharlestonWebpage** repository. Use only this repository; do not create a new one. GitHub Pages from a private repository requires an eligible paid plan; free hosting uses a public repository.
2. Upload the **contents** of this folder to the repository root, including index.html, guide.html, the Markdown and CSV files, the alternate map file, CNAME and the empty .nojekyll file. Do not upload the ZIP itself or nest the files inside a github-pages folder.
3. In repository **Settings → Pages**, choose **Deploy from a branch**, **main**, and **/(root)**, then save.
4. The custom-domain field should be **forensiclawoffice.com**, matching CNAME. Configure the domain before changing DNS.
5. After DNS and the certificate are ready, enable **Enforce HTTPS**. Open the published URL on your phone and bookmark it or use your browser's Add to Home Screen command.

If you want the default address first, omit CNAME and leave the custom-domain field empty. The expected address after deployment is https://ncmsec.github.io/CharlestonWebpage/ . This is an expected URL, not a claim that deployment has completed.

[GitHub's publishing instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

## DNS for forensiclawoffice.com

In Cloudflare, open **forensiclawoffice.com → DNS → Records** and configure these website records. For this initial setup, use **DNS only** (gray cloud) and **Auto** TTL so traffic goes directly to GitHub Pages.

| Type | Name / Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | ncmsec.github.io |

Replace conflicting website records for @ or www; preserve unrelated email MX/TXT records. Check any existing AAAA records for conflicts. GitHub recommends verifying domain ownership in account settings. Allow DNS and HTTPS provisioning to complete; HTTPS can take up to 24 hours.

[GitHub's custom-domain instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

[Cloudflare record controls](https://developers.cloudflare.com/dns/manage-dns-records/how-to/create-dns-records/) · [Cloudflare proxy status](https://developers.cloudflare.com/dns/proxy-status/)

## Files and updates

- **index.html** — map homepage; embedded map libraries, street geometry and 99 place records.
- **charleston-walking-map.html** — identical map under its downloadable filename.
- **guide.html** — readable guide with jump links and mobile table scrolling.
- **charleston-walking-guide.md** — complete original Markdown guide.
- **charleston-places.csv** — place list with coordinates and links.
- **CNAME** — chosen domain.
- **.nojekyll** — publishes the files directly.

Publishing makes the Airbnb address, event schedule and itinerary publicly accessible; explicit stay dates have been removed from page titles and headers. The local downloaded map works offline; venue links, directions and the optional online basemap require internet. A hosted page is not guaranteed to remain available offline merely because it was opened once.

When updating the map, keep index.html and charleston-walking-map.html identical. When editing the guide, update both the Markdown and readable HTML versions. No reservations or purchases have been made. Research checked September 17, 2026; revisit venue and event links before traveling.

MedQ – Supporting Files
=======================

This ZIP contains supporting files only. It intentionally does NOT contain or modify your uploaded HTML file.

Target site URL used in robots.txt and sitemap.xml:
https://medq-daily.netlify.app

Files:
- ads.txt: Google AdSense seller declaration using the publisher ID found in your HTML.
- robots.txt: allows crawling and points crawlers to sitemap.xml.
- sitemap.xml: lists the homepage only. Your current app is a single-page interface, so hidden tabs are not separate crawlable URLs.
- manifest.json: PWA metadata referenced by your HTML.
- sw.js: service worker referenced by your HTML. It uses network-first navigation with an offline cached-shell fallback.
- favicon.ico: browser favicon fallback.
- icons/: 192px and 512px app icons referenced by manifest.json.

Deployment:
1. Keep your original HTML file unchanged and rename it to index.html.
2. Put index.html and all files/folders from this ZIP together in the Netlify publish/root directory.
3. Deploy the site.
4. Check these URLs after deployment:
   - https://medq-daily.netlify.app/ads.txt
   - https://medq-daily.netlify.app/robots.txt
   - https://medq-daily.netlify.app/sitemap.xml
   - https://medq-daily.netlify.app/manifest.json
5. In Google Search Console, submit sitemap.xml if you use Search Console.
6. In AdSense, check the ads.txt status. Google notes that its status can take time to refresh.

Important checks:
- The publisher ID above was read from the AdSense script in the uploaded HTML. Confirm it matches the ID shown in your AdSense account before publishing.
- The HTML itself contains medq-daily.netlify.app in its built-in Privacy Policy and Contact information. The sitemap/robots URLs use that same hostname. If the actual deployment hostname differs, update those URL references in robots.txt and sitemap.xml before deployment, and separately update the HTML's visible policy/contact URLs when you are ready.
- Your HTML currently loads the AdSense library but has no explicit ad-unit slot markup. This is compatible with an Auto ads setup if Auto ads is enabled for the site in AdSense; this ZIP does not change ad settings.
- manifest and service worker support the references already present in your HTML; they do not add new question-bank code or split your HTML.

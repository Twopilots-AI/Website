# twopilots.ai — deploy

Upload the contents of this folder to the web root. Nothing needs building.

    index.html              the site
    favicon-32.png          browser tab
    apple-touch-icon.png    iOS home screen
    icon-512.png            high-DPI / PWA
    og.png                  link preview card (Slack, LinkedIn, WhatsApp, iMessage)
    mark.png                the ring mark, for the email signature
    robots.txt              search engines
    sitemap.xml             one URL; update lastmod when the page changes

## After it is live

1. Confirm both hostnames serve the site:
   https://twopilots.ai  and  https://www.twopilots.ai
   Both already resolve to the same addresses. Pick one as canonical and
   301-redirect the other, so search engines do not index two copies.

2. Confirm https works and http redirects to it.

3. Test the link preview. Paste the URL into Slack and into LinkedIn's
   post composer. If the old blank preview is cached, use
   https://www.linkedin.com/post-inspector/ to force a refresh.

4. Switch on the logo in the email signature. In
   twopilots_email_signature.html, add this line inside the signature
   table, directly above the name row:

       <tr><td style="padding-bottom:10px"><img src="https://twopilots.ai/mark.png"
       width="34" height="29" alt="twopilots.ai"></td></tr>

## Known items

- Fonts load from Google Fonts. Fine on a hosted site. If you ever need the
  page to work offline, download Newsreader and Inter, serve them from
  /fonts, and replace the <link> with @font-face rules.
- The team section is placeholder text. Do not deploy with "Name" showing —
  either fill in the real bios or delete the section and its nav link first.
- og:url, og:image and the sitemap all point at the apex domain. If you make
  www canonical instead, update those three.

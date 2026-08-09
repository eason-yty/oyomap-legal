# Oyomap Legal & Support

Public static pages for Oyomap, hosted with GitHub Pages.

| Route | Purpose |
|---|---|
| `/` | Legal and support landing page |
| `/privacy/` | Public privacy policy for the app and App Store Connect |
| `/support/` | Public support URL for App Store Connect |
| `/terms/` | Apple Standard EULA link plus Oyomap supplemental terms |

## Deployment

The site is plain HTML/CSS and deploys from the root of `main`. It has no build step, JavaScript, cookies, analytics, or secrets.

Production URL: `https://www.oyomap.com/`

Fallback Pages URL: `https://eason-yty.github.io/oyomap-legal/`

The `CNAME` file and Cloudflare DNS records target `www.oyomap.com`. The apex domain uses GitHub Pages' four documented A records, and `www` is a DNS-only CNAME to `eason-yty.github.io`. Existing Cloudflare Email Routing MX, SPF, and DKIM records must remain untouched.

## Launch checklist

| Owner | Action | Done when |
|---|---|---|
| Founder | Review the policy and terms; obtain legal review if desired | Public wording is approved |
| Founder | Configure and test `support@oyomap.com` and `privacy@oyomap.com` forwarding | Both addresses receive and can answer test mail |
| Firebase | Set and verify Analytics event-data retention at no more than 14 months | GA property setting matches the policy |
| Founder | Choose a support/feedback retention routine | Old Asana/email requests are deleted or anonymized when no longer needed |
| DNS | Verify `oyomap.com` in GitHub and point `www` to `eason-yty.github.io` | GitHub domain check succeeds |
| Repository | Add a `CNAME` containing `www.oyomap.com`, then enable HTTPS | `https://www.oyomap.com/` loads without warnings |
| App | Point the in-app Privacy and Terms links to the final HTTPS routes | Release archive opens both links |
| App Store Connect | Enter the final Privacy Policy and Support URLs; answer App Privacy consistently | Metadata matches the shipped app and policy |

For the custom domain, use GitHub's current Pages instructions. Typically `www` is a CNAME to `eason-yty.github.io`; GitHub recommends also securing the apex domain against takeover. Do not change mail-related MX records when configuring the website.

## Content maintenance

Update the effective date and policy whenever collection, providers, account/cloud behavior, advertising, or subscription behavior materially changes. Recheck the app, `PrivacyInfo.xcprivacy`, Firebase settings, App Store Connect answers, and this site together before every release.

# Email Signatures — Agent Marketing Desk

Self-hosted email signatures for Agent Marketing Desk clients. Each client gets their own folder with their signature HTML and images.

## Structure

```
clients/
  <client-name>/          # kebab-case, e.g. karen-duong
    signature.html        # the signature to copy into the email client
    images/               # client-specific images (headshot, brokerage logo, etc.)
shared/
  images/                 # shared assets used across signatures (contact icons, sign-off gif)
```

## Adding a new client

1. Create `clients/<client-name>/` with an `images/` subfolder
2. Copy an existing `signature.html` as a starting point and update name, title, contact info, links, and images
3. Put client-specific images (headshot, logo) in `clients/<client-name>/images/`
4. Reference images via raw GitHub URLs:
   - Client images: `https://raw.githubusercontent.com/Agent-Marketing-Desk/email-signature/main/clients/<client-name>/images/<file>`
   - Shared icons: `https://raw.githubusercontent.com/Agent-Marketing-Desk/email-signature/main/shared/images/<file>`
5. Commit and push — images are served from GitHub raw URLs, so they're live after push

## Installing a signature

1. Open the client's `signature.html` in a browser
2. Select all (Cmd+A) and copy (Cmd+C)
3. Paste into the email client's signature settings

### Gmail
Settings → See all settings → General → Signature → Paste

### Outlook (Desktop)
File → Options → Mail → Signatures → Paste

### Outlook (Web)
Settings → Mail → Compose and reply → Email signature → Paste

## Notes

- This repo must stay **public** — email clients load the images from raw GitHub URLs
- Don't rename or delete images that deployed signatures reference; email clients keep the old URLs

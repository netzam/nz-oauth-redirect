# nz-oauth-redirect

Minimal GitHub Pages site for OAuth callback redirects.

## Purpose
This page receives OAuth redirect parameters (`?code=...` and/or `#access_token=...`), displays them for debugging, and forwards them to the opener window via `postMessage` for popup-based login flows.

## Live URL
After Pages is enabled:

`https://netzam.github.io/nz-oauth-redirect/`

## Security notes
- The example uses `postMessage(..., "*")` for compatibility.
- In production app code, always validate `event.origin` on the receiver side.
- If needed, restrict target origin in this page to your app domain.

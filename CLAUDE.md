# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**This site is now a redirect.** Dataplex was rebranded as **Cogniplex** (new site: [cogniplex.es](https://cogniplex.es), repo `cogniplexai/cogniplex-web`). Every page here is a lightweight client-side redirect (canonical link + `meta refresh 0` + JS `location.replace`) to the equivalent page on cogniplex.es:

| Page | Redirects to |
|---|---|
| `index.html` | `https://cogniplex.es/` |
| `aviso-legal.html` | `https://cogniplex.es/aviso-legal/` |
| `privacidad.html` | `https://cogniplex.es/privacidad/` |
| `cookies.html` | `https://cogniplex.es/cookies/` |
| `404.html` | `https://cogniplex.es/` (catch-all for any unknown path) |

Client-side redirect (instead of a registrar 301) was chosen deliberately: it keeps the dataplex.es DNS zone untouched (it carries Proton Mail MX/SPF records that must not be disturbed) and keeps serving `https://dataplex.es` with GitHub Pages' valid TLS certificate.

## Development

No build step. **Deployment:** push to `main` and GitHub Pages auto-deploys to `dataplex.es` (configured via the `CNAME` file — do not delete it, nor `.nojekyll`).

## Git Workflow

The maintainer works solo and prefers a fully automated branch → PR → merge → back-to-main cycle. Drive it end to end; the only manual step expected from the user is approving the merge (or saying "hazlo tú").

For any non-trivial change:
1. Create a new branch off `main` automatically — do not ask first.
2. Make the changes and show the result.
3. Open the PR with `gh pr create`.
4. After the merge, delete the branch (local + remote) and return to `main` without being asked.

Trivial one-line tweaks may go straight to `main`. When in doubt, branch.

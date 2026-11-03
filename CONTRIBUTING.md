# Contributing to email-router-api

Thank you for your interest in contributing. We welcome contributions that optimize edge routing rules, improve MIME construction, or enhance CORS security.

## Edge Development Invariants
When modifying `worker.js`:
1. **Cloudflare Worker Runtime Standards**: Code must strictly execute within the V8 isolates environment without relying on Node.js-only native binaries.
2. **Header Sanitization**: Any new field rendered into email headers must sanitize CRLF sequences.
3. **Zero Hardcoded Secrets**: Use Cloudflare environment bindings (`env.SEND_EMAIL`) for secret and service access.

## Contribution Workflow
1. Fork and clone:
   ```bash
   git clone https://github.com/<your-username>/email-router-api.git
   cd email-router-api
   ```
2. Test locally using Wrangler:
   ```bash
   npm run dev
   ```
3. Submit a Pull Request completing the mandatory security checklist in `.github/PULL_REQUEST_TEMPLATE.md`.
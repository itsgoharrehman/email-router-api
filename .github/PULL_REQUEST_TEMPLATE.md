## Summary of Changes

Describe the proposed changes, edge routing impact, and reason for the modification.

## Quality and Security Checklist

Before submitting this pull request, verify each of the following invariants:

- [ ] **CRLF Sanitization**: Verified that all inputs rendered to email headers are stripped of `\r` and `\n` characters.
- [ ] **Edge Compatibility**: Verified that code executes within the Cloudflare Workers V8 runtime without Node-only dependencies.
- [ ] **No Hardcoded Secrets**: Verified that no Cloudflare API keys or private email addresses are committed.
- [ ] **Tested with Wrangler**: Verified locally via `npm run dev`.

## Testing Performed

Detail the local tests or manual verification steps conducted.
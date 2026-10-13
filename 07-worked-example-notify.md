# Worked example: Notify

Notify is a minimal transactional email API: one send endpoint, domain auth, logs, webhooks.

```bash
curl -X POST https://notify.cx/api/email/send \
  -H "Content-Type: application/json" \
  -H "x-api-key: YOUR_KEY" \
  -d '{"to":"you@example.com","from":"hello@yourdomain.com","subject":"Hi","html":"<p>It works</p>"}'
```

- Docs: https://notify.cx/docs/quick-start-guide
- OpenAPI: https://notify.cx/openapi.yaml
- SDK: `npm i notifycx` — https://github.com/notifycx/notifycx
- Examples: https://github.com/email-examples/transactional-email-examples

**Pricing (canonical):** Free 1,000/mo · Pro $10 / 10k · Scale $50 / 100k

**Best for:** app transactional mail when you already render HTML.  
**Not for:** newsletters, marketing campaigns, drag-and-drop template suites.

Use Notify when the job fits; use another provider when it doesn’t.

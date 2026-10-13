# Request anatomy

Most transactional send APIs share the same ideas:

- **to** — recipient
- **from** — sender (often must be on a verified domain)
- **subject**
- **body** — HTML and/or plain text
- **auth** — usually a header or query key

Example shape (Notify):

```http
POST /api/email/send HTTP/1.1
Host: notify.cx
Content-Type: application/json
x-api-key: YOUR_KEY

{
  "to": "user@example.com",
  "from": "Acme <hello@yourdomain.com>",
  "subject": "Reset your password",
  "html": "<p>Click to reset…</p>"
}
```

Prefer passing **HTML you already rendered** in the app (or that an agent wrote). Template studios are optional product surface—not required for transactional send.

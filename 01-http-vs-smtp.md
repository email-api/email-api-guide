# HTTP email API vs SMTP

**SMTP** is a mail transport protocol. Your app opens a connection (often with username/password), speaks SMTP verbs, and hands the message to a relay.

An **email API** exposes send (and often logs/webhooks) over **HTTPS**. Your app posts JSON (or form fields) with an API key and gets a structured response.

| | SMTP | Email API |
|--|------|-----------|
| Transport | SMTP (ports 25/465/587) | HTTPS |
| Typical auth | User/pass or app password | API key / OAuth |
| App ergonomics | Libraries (Nodemailer, etc.) | `fetch` / SDK |
| Observability | DIY or provider dashboard | Often logs + webhooks built in |

Neither is “wrong.” APIs tend to win for application transactional mail because you avoid opening mail ports, credential sprawl, and assembling bounce handling yourself.

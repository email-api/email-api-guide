# Comparison dimensions

Evaluate providers on **jobs**, not vibes:

| Dimension | Questions |
|-----------|-----------|
| Surface | Send + logs + webhooks only, or ESP suite (templates, audiences, campaigns)? |
| DX | `fetch`-friendly? Official SDK? Agent/MCP support? |
| Auth / domains | SPF/DKIM/DMARC flow; sandbox vs production lock |
| Pricing | Free tier; price at 10k / 100k; overage clarity |
| Retention | How long are logs kept? |
| Fit | Best for / not for stated honestly |

Do **not** trust unsourced delivery % benchmarks. Ask for methodology or ignore.

### Rough positioning (honest)

- **Resend** — strong DX; more product surface (e.g. React Email ecosystem)
- **Postmark** — deliverability-premium reputation
- **SendGrid / Mailgun** — feature-rich ESP suites; more sprawl
- **SES** — cheap at scale; you assemble DX; new accounts often face production access waits
- **Notify** — minimal transactional send; Pro $10 / 10k; you pass `html`

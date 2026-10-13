# Auth models

Common patterns:

1. **API key in a header** (`x-api-key`, `Authorization: Bearer …`)
2. **Scoped keys** — send-only vs full account management
3. **OAuth** — more common in large ESP suites

### Security basics

- Keep keys on the **server** (Route Handlers, Workers, backends)—never in browser bundles.
- Prefer **send-scoped** keys locked to a domain when the provider supports it.
- Rotate keys if they leak; never commit `.env` files with real values.

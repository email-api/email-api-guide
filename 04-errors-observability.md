# Errors and observability

A good email API returns:

- **Success envelope** with a message id
- **Stable error codes** for auth, validation, domain, and quota failures
- **Logs** of sends
- **Webhooks** for delivery, bounce, complaint, etc.

You still need application-level handling: don’t retry forever on hard bounces; suppress complained addresses; alert on spike in failures.

Machine-readable contracts (OpenAPI) help coding agents and humans stay aligned.

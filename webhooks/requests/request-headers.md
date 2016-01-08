# Request Headers

All Webhook requests are delivered with a set of HTTP headers detailing context about the event.

| Header | Description |
|--------|--------------|
| **layer-webhook-event-type** | Type of event that triggered delivery. |
| **layer-webhook-signature** | The computed HMAC hex digest of the body, using the configured **secret** as the key. |
| **layer-webhook-request-id** | A unique ID (UUID) for this Webhook request. This ID will be reused if this particular request needs to be resent to your server. |
| **layer-webhook-id** | The ID (UUID) of the webhook. |
| **user-agent** | `layer-webhooks/1.0` |
| **content-type** | `application/json` |

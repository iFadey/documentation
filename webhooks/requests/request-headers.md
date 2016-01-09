# Request Headers

All Webhook requests are sent to your server with the following headers:

| Header | Description |
|--------|--------------|
| **layer-webhook-event-type** | [Event Type](introduction#event-types) that triggered this request to your server. |
| **layer-webhook-signature** | The computed HMAC hex digest of the body, using the configured **secret** as the key. |
| **layer-webhook-request-id** | A unique ID (UUID) for this Webhook request. This ID will be reused if this particular request needs to be resent to your server. |
| **layer-webhook-id** | The ID (UUID) of the webhook. |
| **user-agent** | `layer-webhooks/1.0` |
| **content-type** | `application/json` |

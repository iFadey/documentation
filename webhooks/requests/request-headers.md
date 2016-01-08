# Request Headers

All Webhook requests are delivered with a set of HTTP headers detailing context about the event.

| Header | Description |
|--------|--------------|
| `layer-webhook-event-type` | Type of event that triggered delivery. |
| `layer-webhook-signature` | The computed HMAC hex digest of the body, using the configured `secret` as the key. |
| `layer-webhook-request-id` | A unique ID (UUID) for this Webhook request. |
| `layer-webhook-id` | The ID (UUID) of the webhook. |

* Requests will have a `User-Agent` of `layer-webhooks/1.0`.
* Requests will have a `Content-Type` of `application/json`.

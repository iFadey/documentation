# Create a Webhook

| Name    | Type   | Description |
|---------|:------:|-------------|
| `target_url`    | string   | Destination URL for the webhook (must be HTTPS) |
| `event_types` | array of strings | Types of [events](#introduction/event-types) that will cause this webhook to be triggered |
| `secret` | string  | String that’s passed with the HTTP requests as a `layer-webhook-signature` header. The value of this header is computed as the HMAC hex digest of the body, using the secret as the key. |
| `target_config`   | dictionary   | A free form dictionary of supplemental data specific to the webhook |

```request
POST https://api.layer.com/apps/:app_id/webhooks
```

```json
{
    "target_url": "https://client.example.com/layeruser/foo",
    "event_types": [
      "user.registered",
      "conversation.created"
    ],
	"secret": "1697f925ec7b1697f925ec7b"
	"target_config" : {
		"key1" : "value1",
		"key2" : "value2"
	}
}
```

### Response `201 (Created)`

```json
{
    "id": "layer:///apps/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/f5ef2b54-0991-11e5-a6c0-1697f925ec7b",
	"url": "https://api.layer.com/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/f5ef2b54-0991-11e5-a6c0-1697f925ec7b"
    "target_url": "https://client.example.com/layeruser/foo",
    "event_types": [
      "user.registered",
      "conversation.created"
    ],
    "status": "unverified",
    "created_at": "2015-03-14T13:37:27Z",
	"target_config" : {
		"key1" : "value1",
		"key2" : "value2"
	}
}
```

Note that this results in an `unverified` webhook; the webhook must be verified before it receives events.

### Secrets

The `secret` specified when a Webhook is created is used to compute a [Hash-based Message Authentication Code](http://en.wikipedia.org/wiki/HMAC) (or HMAC) over the serialized request body before it is sent. The HMAC is delivered with the request via the `layer-webhook-signature` HTTP header.

When integrating a Layer Webhook with your application, it is recommended that you verify the integrity of the payload by validating the signature given in the `layer-webhook-signature` header. You can do so by feeding the secret and complete request body to a crypto library (such as OpenSSL) that is capable of computing an HMAC digest. If the request is valid and the body has not been tampered with, the computed signature will match the header value exactly.


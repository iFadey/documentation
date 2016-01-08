# Create a Webhook

| Name    | Type   | Description |
|---------|:------:|-------------|
| `target_url`    | string   | Destination URL for the webhook (must be HTTPS) |
| `event_types` | array of strings | Types of [events](#event-types) that will cause this webhook to be triggered |
| `secret` | string  | String that’s passed with the HTTP requests as an `layer-webhook-signature` header. The value of this header is computed as the HMAC hex digest of the body, using the secret as the key. |
| `target_config`   | dictionary   | A free form dictionary of supplemental data specific to the webhook | 

```
POST https://api.layer.com/apps/{app_id}/webhooks
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

> 201 Created  {
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
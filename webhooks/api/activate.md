# Activate a Webhook

```
POST https://api.layer.com/apps/{app_id}/webhooks/{webhook_id}/activate

> 200 OK {
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

If the webhook status is `unverified` or `inactive`, this results in a verification challenge being sent to the `target_url`.  The webhook status will transition to `active` once verification completes successfully.

This is a no-op if the webhook status is already `active`.

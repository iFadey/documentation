# Get a Webhook by ID

You can get the details and status of a single webhook by requesting it from the API:

```request
GET https://api.layer.com/apps/:app_id/webhooks/:webhook_id
```

### Response `200 (OK)`

```json
{
    "id": "layer:///apps/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/f5ef2b54-0991-11e5-a6c0-1697f925ec7b",
	"url": "https://api.layer.com/apps/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/f5ef2b54-0991-11e5-a6c0-1697f925ec7b",
    "target_url": "https://mydomain.com/my-webhook-endpoint",
    "event_types": [
      "user.registered",
      "conversation.created"
    ],
    "status": "active",
    "created_at": "2015-03-14T13:37:27Z",
	"target_config" : {
		"key1" : "value1",
		"key2" : "value2"
	}
}
```

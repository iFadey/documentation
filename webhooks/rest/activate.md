# Activate a Webhook

If the webhook status is `inactive`, you can use this API to start the process of reactivating it.  Activating an inactive webhook is a two step process:

1. **Call the activate endpoint**: Sets the webhook status to `unverified`.
2. **Verify the webhook**: The [Verification Step](#verify) is automatically started and if completed successfully, sets the webhook status to `active`.

Failing to complete the [Verification Step](#verify) will cause your webhook status to revert to `inactive`.

```request
POST https://api.layer.com/apps/:app_id/webhooks/:webhook_id/activate
```

### Response `200 (OK)`

```json
{
    "id": "layer:///apps/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/f5ef2b54-0991-11e5-a6c0-1697f925ec7b",
	"url": "https://api.layer.com/apps/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/f5ef2b54-0991-11e5-a6c0-1697f925ec7b"
    "target_url": "https://mydomain.com/my-webhook-endpoint",
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

# List Webhooks

You can request a list of all of your webhooks from the API:

```request
GET https://api.layer.com/apps/:app_id/webhooks
```
### Response `200 (OK)`

```json
[
  {
    "id": "layer:///apps/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/f5ef2b54-0991-11e5-a6c0-1697f925ec7b",
	"url": "https://api.layer.com/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/f5ef2b54-0991-11e5-a6c0-1697f925ec7b"
    "target_url": "https://client.example.com/layeruser/foo",
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
  },
  {
    "id": "layer:///apps/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/g6ef2b54-0991-11e5-a6c0-1697f925ec7a",
	"url": "https://api.layer.com/082d4684-0992-11e5-a6c0-1697f925ec7b/webhooks/g6ef2b54-0991-11e5-a6c0-1697f925ec7a"
    "target_url": "https://client.example.com/layeruser/foo",
    "event_types": [
      "conversation.deleted"
    ],
    "status": "inactive",
	"created_at": "2015-05-14T13:37:27Z",
	"target_config" : {}
  }
]
```
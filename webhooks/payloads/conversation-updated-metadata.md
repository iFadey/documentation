# Conversation Metadata Change

A `conversation.updated.metadata` event is sent whenever there is a change to any Conversation's metadata.  The event is triggered for changes made by users and by the Platform API.

```json
{
	"event_timestamp": "2015-09-17T20:46:47.561Z",
	"event_type": "conversation.updated.metadata",
	"event_id": "c12f340d-3b62-4cf1-9b93-ef4d754cfe69",
	"conversation": {
	    "id": "layer:///conversations/f3cc7b32-3c92-11e4-baad-164230d1df67",
		"url": "https://api.layer.com/apps/082d4684-0992-11e5-a6c0-1697f925ec7b/conversations/e67b5da2-95ca-40c4-bfc5-a2a8baaeb50f",
	    "created_at": "2014-09-15T04:44:47+00:00",
		 "messages_url": "https://api.layer.com/apps/082d4684-0992-11e5-a6c0-1697f925ec7b/conversations/c12fd916-1390-464b-850f-1380a051f7c8/messages",
	    "distinct": false,
	    "participants": [
	        "1234",
	        "5678"
	    ],
	    "metadata": {
	    	"favorite": "true",
	    	"background_color": "#3c3c3c"
	    }
	},
	"target_config" : {
		"key1" : "value1",
		"key2" : "value2"
	}
}
```
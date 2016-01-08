# `message.sent`

Triggered when a new Message is sent.

```json
{
	"event_timestamp":"2015-09-17T20:46:47.561Z",
	"event_type":"message.sent",
	"event_id":"c12f340d-3b62-4cf1-9b93-ef4d754cfe69",
	"message": {
	    "id": "layer:///messages/940de862-3c96-11e4-baad-164230d1df67",
	    "conversation": {
	    	"id": "layer:///conversations/e67b5da2-95ca-40c4-bfc5-a2a8baaeb50f",
	    	"url": "https://api.layer.com/apps/082d4684-0992-11e5-a6c0-1697f925ec7b/conversations/e67b5da2-95ca-40c4-bfc5-a2a8baaeb50f"
	    },
	    "parts": [
	        {
	        	"id": "layer:///messages/940de862-3c96-11e4-baad-164230d1df67/parts/0",
	            "mime_type": "text/plain",
	            "body": "This is the message.",
	            "size": 20
	        },
	        {
	            "mime_type": "image/png",
	            "content": {
	           	"id": "layer:///messages/940de862-3c96-11e4-baad-164230d1df67/parts/1",
	                "download_url": "http://google-testbucket.storage.googleapis.com/some/download/path",
	                "expiration": "2014-09-09T04:44:47+00:00",
	                "refresh_url": "https://api.layer.com/content/7a0aefb8-3c97-11e4-baad-164230d1df67",
	                "size": 172114124
	            },
	            "size": 172114124
	        }
	    ],
	    "sent_at": "2014-09-09T04:44:47+00:00",
	    "sender": {
			"user_id": "12345"
	    },
	    "recipient_status": {
	        "12345": "read",
	        "999": "sent",
	        "111": "sent"
	    }
	},
	"target_config" : {
		"key1" : "value1",
		"key2" : "value2"
	}
}
```
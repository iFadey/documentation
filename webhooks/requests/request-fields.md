# Request Fields

Every event comes with the following properties:

| Name | Description |
|--------|--------------|
| **event_timestamp** | Time at which the change being reported on occurred |
| **event_type** | One of the [Event Types](introduction#event-types) |
| **event_id** | Each request has an Event ID which can be used for deduplication in case a request gets resent to your server. |

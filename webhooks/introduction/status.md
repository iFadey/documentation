# Status

Every webhook created has three possible values:

| Status | Description |
|--------|--------------|
| **unverified** | A newly created webhook that is not yet active |
| **active**     | A webhook that is active and receiving events from Layer as they occur |
| **inactive** | A webhook that is no longer active and no longer receiving events |

A newly created webhook will have the status on `unverified`. A webhook that no longer responds when Layer sends them events will change to `inactive`.  Please see [verify the webhook section](rest#verify-the-webhook) for additional details.

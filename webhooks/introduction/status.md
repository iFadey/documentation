# Status

Every webhook created has three possible status values:

| Status | Description |
|--------|--------------|
| **unverified** | A newly created webhook that will not be active until verified. |
| **active**     | A webhook that is active and sending events to your server. |
| **inactive** | A webhook that is no longer active and no longer sending events. |

A newly created webhook will have the status on `unverified`. A webhook that no longer responds when Layer sends events will change to `inactive`.  Please see [verify the webhook section](rest#verify-the-webhook) for additional details.

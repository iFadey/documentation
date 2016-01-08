# Event Types

When configuring a webhook, you choose the events for which you would like to receive payloads by subscribing to the specific events you intend to handle.

Each event type corresponds to a specific action that can occur within your Layer application. The current set of available event types are:

| Event | Description |
|--------|--------------|
| `message.sent` | When a Message is sent. |
| `message.delivered` | When a client acknowledges delivery of a Message. |
| `message.read` | When a client marks a Message as read. |
| `message.deleted` | When a client deletes a Message (Global deletion mode only). |
| `conversation.created` | When a new Conversation is created. |
| `conversation.updated.participants` | When a Conversation's set of participants is updated. |
| `conversation.updated.metadata` | When a Conversation's metadata is updated. |
| `conversation.deleted` | When a Conversation is deleted (Global deletion mode only). |

# Introduction

There are two ways to create and configure your webhooks:

1. The Developer Dashboard
2. The REST API

This section describes the REST API for creating, verifying, listing, disabling and deleting your webhooks.

To get started, your going to want to create a webhook, a process which has two steps.

1. **Create the webhook**: Creates a new webhook with status `unverified`.
2. **Verify the webhook**: Sets the webhook status to `active`; it now sends events to your server.

Before going into detail on creating webhooks, you'll need to be able to send authenticated requests to the API.
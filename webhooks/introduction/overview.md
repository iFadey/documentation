# Overview

Webhooks allow you to develop integrations which subscribe to events within your Layer application.  When a subscribed event is triggered, Layer will send an HTTP POST payload to the endpoint designated in the webhook configuration.  Webhooks provide a simple, flexible mechanism that you can use to signal an external system to take action in response to messaging activity within your app.  You can use Webhooks to implement things like:

* Add context to conversations: respond to messages mentioning keywords
* Notify another user when they are @mentioned
* Integrate a third-party service (Uber API, Weather Underground, etc) into conversations based on context


### Requirements

You must have a webserver able to receive HTTP/1.1 requests and able to support keepalive requests.
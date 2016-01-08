# Responding to a Webhook

The endpoint receiving the Layer webhook is expected to respond with a 2xx status code in order to acknowledge delivery of the request.  Any non-2xx response will be considered a delivery failure.

**NOTE: Your server must respond within 1 second.**  Performant handling and uptime is of utmost importance when it comes to handling webhooks.

**NOTE: Your server must support HTTP/1.1 and keepalive.**  The cost of establishing a new connection with each request flies in the face of performant webhooks.  In the future, we will likely transition to supporting HTTP/2 to eliminate head-of-line blocking and improve throughput for high-volume applications.  For now, HTTP/1.1 is the barrier to entry for webhooks.

Failures will be retried with exponential backoff delay for a period of up to approximately 30 minutes.
 
Retries will have the same value for the `layer-webhook-request-id` header, and the target server must be able to handle duplicate transmissions of webhook requests.

If the webhook request fails to get a response after the retry period expires, the webhook will be transitioned to `inactive` status.  From there, it may be reactivated using the activation API.  The Web UI will also display the reason when a webhook is deactivated.

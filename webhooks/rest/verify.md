# Verify the Webhook

The first request to your new webhook URL will be a verification request to confirm that Layer is communicating with the correct service.  This helps to avoid your information from leaking to unintended recipients.

The verification request will be a `GET` request with a `verification_challenge` query string parameter.  Its value will be a random string.  Your service should echo back the challenge parameter in the response body.  Once Layer receives a valid response, the endpoint is considered to be a valid webhook, and Layer will begin sending notifications to that endpoint.  Layer will not attempt to retry the verification request, and your webhook becomes `inactive`.

NOTE: The `Content-Type` in your response to the verification challenge is not important and will be ignored.

```request
GET https://client.yourdomain.com/layeruser/foo?verification_challenge=de7c9b85b8b78aa6bc8a7a36f70a90701c9db4d9
```

### Response `200 (OK)`

```
de7c9b85b8b78aa6bc8a7a36f70a90701c9db4d9
```

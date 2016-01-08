# Validating Payload Integrity

The `secret` specified when a Webhook is created is used to compute a [Hash-based Message Authentication Code](http://en.wikipedia.org/wiki/HMAC) (or HMAC) over the serialized request body before it is sent.  The HMAC is delivered with the request via the `layer-webhook-signature` HTTP header.

When integrating a Layer Webhook with your application, it is recommended that you verify the integrity of the payload by validating the signature given in the `layer-webhook-signature` header.  You can do so by feeding the `secret` and complete request body to a crypto library (such as OpenSSL) that is capable of computing an `HmacSHA1` digest.  If the request is valid and the body has not been tampered with, the computed signature will match the header value exactly.

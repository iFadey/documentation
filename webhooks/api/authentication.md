# Authentication

Authentication for the Webhooks API is based on a token generated from within the developer dashboard (same token as the Platform API).  This token can be generated with an expiry period (not currently supported, planned feature) and/or revoked.

The token needs to be included in the `Authorization` header of each HTTP request as follows:

```
Authorization: Bearer x32pYli9DCBByPUzz3CMLU9jDTYdiAacNiJrMIkdp4lTf6sb
```

If the token is missing or invalid, the server will respond with `401 Unauthorized`.

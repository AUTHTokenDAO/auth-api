## AUTH Token API

This contains the OpenAPI specifications for the AUTH Token API, see the
[complete AUTH API documentation](https://authtokendao.github.io/auth-api/).



### Webhook Callbacks

NOTE: The above API does not include the webhook callbacks that are made upon successful
AUTH redemptions and other state changes relevant to vendors. This should be orchestrated
by something like https://temporal.io/.

#### AUTH Redemption Vendor Callback

Example data sent on a POST webhook callback after AUTH redemption to `https://somevendor.com/redeem-callback`:

```json
{
  "verification_code": "XXXXX",
  "wallet": "solanawalletaddress",
  "email": "me@wenlambo.com",
  "redeemed_utc": "2022-01-01T01:23:45Z",
  "expiry_utc": "2024-01-01T01:23:45Z",
  "reward_units": 10,
  "duration_weeks": 104
}
```

# Create Link FN

## Development

- cp .env.example .env

- edit .env

```toml
PAYMONGO_EMAIL=
PAYMONGO_PASS=
PAYMONGO_LIVE_MODE=
```

- run `netlify dev` command

- test http://localhost:8888/api in postman

<details>
  <summary>Raw JSON PAYLOAD</summary>
 
```json
{
    "amount": 100000,
    "description": "iPhone Xfinity (1)",
    "livemode": false,
    "remarks": "test"
}
```
- **NOTE: Call This upon Checkout**

- amount is required , and is on cents. i.e.: **100000 = 1000.00 php**

- description is required , and is your Order Details **format: product_name (QTY)** provided by cart system.

- livemode is set as ENV variable, Set it to **true** if you have active paymongo account

- remarks is optional 
</details>

## Deploy
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/thriftshop-fn/create-link)

## Set Your Domain In Netlify

- Go to [Settings](https://app.netlify.com/sites/tss-test/settings/general)

- Click Change Site Name `${username}-tss-fn-create-link.yourdomain.com`

## Production

- make post request with Needed *payload* to `${username}-tss-fn-create-link.domain.com/api`



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

> *Raw JSON PAYLOAD*
```json
{
		"amount": 100000, // equals 1000.00 PHP
		"description": "Order Details",
		"livemode": false,
		"remarks": "test"
}
```


## Deploy
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/thriftshop-fn/create-link)

## Set Your Domain In Netlify

- Go to [Settings](https://app.netlify.com/sites/tss-test/settings/general)

- Click Change Site Name `${username}-tss-fn-create-link.yourdomain.com`

## Production

- make post request with Needed *payload* to `${username}-tss-fn-create-link.domain.com/api`



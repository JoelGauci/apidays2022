
# Workshop Session: API Security Solution Dojo

![Solution Dojo](img/Google_Cloud_Logo.svg.png)

![Solution Dojo](img/solution-dojo.png)

Welcome to the **API Security Solution Dojo**, where you will experience working
through 3 scenarios to better understand API security concerns...

## Preparing for the challenges

To send API requests, just use a simple HTTP client (like cURL, Postman,...)

## (Very) Important Notes

- Remember that you can use anything at your disposal - laptops, TVs,
phones, your neighbor, or any software you find on the internet (e.g. GitHub),
but do take care not to run any malicious code!

- In this git repo you can find OpenAPI Specification files, which document the APIs for
the challenges

## cURL commands

The cURL commands must be executed from your laptop.

### Free pizza, anyone? - duration: 10 min

```bash

export HOSTNAME=bap.iloveapis.io

export CHALLENGE_KEY=...

curl https://${HOSTNAME}/pizza/v1/orders -X PUT \
-d '{"id": 5124,"order_total": 42.53,"items": ["vegan-stuffed","pepperoni-deep"],"last_updated": 1643383304,"promo_code": null,"payment_status": "PENDING"}' \
-H "X-Challenge-Key: ${CHALLENGE_KEY}"
-H "Content-Type: application/json" -v
```

### Greed is good - duration: 10 min

```bash

export HOSTNAME=bap.iloveapis.io

export CHALLENGE_KEY=...

curl https://${HOSTNAME}/holiday/v1/reserve?package=1234 -X POST \
-d '{"first_night":"2023-01-01","last_night":"2023-12-31","num_adult":2,"num_child":4}' \
-H "X-Challenge-Key: ${CHALLENGE_KEY}" \
-H "Content-Type: application/json" -v
```

### Spinning keys, not plates - duration: 10 min

```bash

export HOSTNAME=bap.iloveapis.io

export CHALLENGE_KEY=...

curl "https://${HOSTNAME}/ecommerce/v1/products?apikey=xkey-asd-spinning-keys-not-plates" \
-H "X-Challenge-Key: ${CHALLENGE_KEY}" -v
```

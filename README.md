
# Workshop Session: API Security Solution Dojo

![Solution Dojo](img/enlarge_apidays_2022.jpeg)

![Solution Dojo](img/Google_Cloud_Logo.svg.png)

![Solution Dojo](img/solution-dojo.png)

Welcome to the **API Security Solution Dojo**, where you will experience working
through 2 scenarios to better understand API security concerns...

## Preparing for the challenges

To send API requests, just use a simple HTTP client (like cURL, Postman,...)

## (Very) Important Notes

- Remember that you can use anything at your disposal - laptops, TVs,
phones, your neighbor, or any software you find on the internet (e.g. GitHub),
but do take care not to run any malicious code!

- In this git repo you can find OpenAPI Specification files, which document the APIs for
the 2 challenges

- You are welcome to visit us at the Google Cloud booth during the apidays 2022 event!!!

## cURL commands

The cURL commands must be executed from your laptop.

### Free pizza, anyone? - duration: 10 min

```bash

export HOSTNAME=apigeex.iloveapis.io

curl https://${HOSTNAME}/pizza/v1/orders -X PUT \
-d '{"id": 5124,"order_total": 42.53,"items": ["vegan-stuffed","pepperoni-deep"],"last_updated": 1643383304,"promo_code": null,"payment_status": "PENDING"}' \
-H "Content-Type: application/json" -v
```

### You crack me up! - duration: 15 min

```bash

export HOSTNAME=apigeex.iloveapis.io

export JWT='eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiI5OTk5OSIsIm5hbWUiOiJQb29yIFZpY3RpbSIsImFkbWluIjpmYWxzZSwiaWF0IjoxNTE2MjM5MDIyfQ.1wOb4doI3_aTxpxtvxrGvBpizJqJuiwjifX5lylZxfw'

curl -H "Authorization: Bearer ${JWT}" \
https://${HOSTNAME}/users/me/accounts/v1/balance -v
```

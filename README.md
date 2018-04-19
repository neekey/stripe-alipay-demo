# stripe-alipay-demo
The demo for integration Alipay with Stripe

API: https://stripe.com/docs/sources/alipay

# Workflow:

- In our end, using `Stripe.createSource()` to create a payment source, within the result, we can get a redirect URL to Alipay
- Redirect the user to Alipay, user will payment the amount and will be redirect back
- Through the back url the source object's `id` and `client_secret` will be attached, we can use these as parameters to invoke `Stripe.retriveSource()` to check the payment status

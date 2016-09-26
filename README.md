# Braintree Flask
[![Build Status](https://travis-ci.org/braintree/braintree_flask_example.svg?branch=master)](https://travis-ci.org/braintree/braintree_flask_example)

An example Braintree integration for python in the Flask framework.

## Setup Instructions

1. Install requirements:
  ```sh
  pip install -r requirements.txt
  ```

2. Copy the `example.env` file to `.env` and fill in your Braintree API credentials. Credentials can be found by navigating to Account > My User > View Authorizations in the Braintree Control Panel. Full instructions can be [found on our support site](https://articles.braintreepayments.com/control-panel/important-gateway-credentials#api-credentials).

3. Start server:
  ```sh
  python app.py
  ```

- The client-side code needs to request a client token from the server, make a braintree.setup call to configure Hosted Fields, and finally present a payment form that uses Hosted Fields.  

- Upon submission, the form should submit a payment method nonce to the server.
 
- On the server side, please make two API calls. The first should use this nonce to verify the card and store it in your vault, and the second should create a transaction using this stored payment method.
 
- The integration should provide feedback indicating whether the the transaction was successful or not.


https://developers.braintreepayments.com/
https://developers.braintreepayments.com/start/overview#client-token
https://developers.braintreepayments.com/guides/hosted-fields/setup-and-integration/javascript/v2#braintree.setup
https://developers.braintreepayments.com/guides/hosted-fields/setup-and-integration/javascript/v2#basic-integration
https://developers.braintreepayments.com/start/overview#payment-method-nonce
https://developers.braintreepayments.com/guides/payment-methods#create
https://developers.braintreepayments.com/guides/transactions

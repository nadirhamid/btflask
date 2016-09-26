# Braintree Flask Example
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

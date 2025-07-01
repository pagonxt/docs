The Web Checkout system can be embedded into your online store in the form of a transparent Checkout in iFrame and Lightbox format, or with the generation of external links for payment in the Redirect URL version.  
For more details on the product, see our GetNet developer portal.

[https://docs.globalgetnet.com](https://docs.globalgetnet.com)

Before testing the APIs, configure some attributes in the Postman environment and select them for consumption.

GetNet APIs base URL  
**host_getnet_api**: fill in `https://api.pre.globalgetnet.com` for the approval environment (PRE) or `https://api.globalgetnet.com` for the production environment (LIVE).

Authentication credentials for the APIs  
**client_id**: obtained from GetNet  
**client_secret**: obtained from GetNet

---

**Authentication**

The collection is set to persist the value of `access_token` automatically on successful execution of the `Create Access Token` endpoint.

---

**Link creation or payment intent**

Enter your order ID in the `order_id` field of the request payload.  
Enter the currency of the merchant's country in the `payment.currency` field, `ARS` for Argentina and `CLP` for Chile.  
For more details on the payload fields, see the API Explorer section of the Web Checkout product on our developer portal.

---

**Post-transaction operations**

The `Refund Payment` and `Cancel Payment` endpoints require a `payment_id` parameter, which must be obtained on receipt of the webhook after payment authorization.  
For more details on the webhook solution, see our developer portal.
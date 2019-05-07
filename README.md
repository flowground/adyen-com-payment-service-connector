# ![LOGO](logo.png) Adyen Payment Service **flow**ground Connector

## Description

A generated **flow**ground connector for the Adyen Payment Service API (version 30).

Generated from: https://api.apis.guru/v2/specs/adyen.com/PaymentService/30/openapi.json<br/>
Generated at: 2019-05-07T17:34:48+03:00

## API Description

A set of API endpoints that allow you to initiate, settle, and modify payments on the Adyen payments platform. You can use the API to accept card payments (including One-Click and 3D Secure), bank transfers, ewallets, and many other payment methods. For more information, refer to [Ecommerce integration](https://docs.adyen.com/developers/ecommerce-integration).

## Authorization

This API does not require authorization.

## Actions

### Adjust the authorised amount

> Allows you to increase or decrease the authorised amount after the initial authorisation has taken place. This functionality enables tipping, improving the chances your authorisation will be valid, charging the shopper when they have already left the merchant premises, etc.<br/>
> <br/>
> For more information, refer to [Adjust Authorisation](https://docs.adyen.com/developers/payment-modifications#adjustauthorisation).

### Create a payment authorisation

> Creates a payment with a unique reference (`pspReference`) and attempts to obtain an authorisation hold. For cards, this amount can be captured or cancelled later. Non-card payment methods typically don't support this and will automatically capture as part of the authorisation.<br/>
> <br/>
> For more information, refer to [Ecommerce quick integration](https://docs.adyen.com/developers/ecommerce-integration).

### Complete a 3D Secure payment authorisation

> For an authenticated 3D Secure session, completes the payment authorisation. This endpoint must receive the `md` and `paResponse` parameters that you get from the card issuer after a shopper pays via 3D Secure.<br/>
> <br/>
> For more information, refer to [3D Secure](https://docs.adyen.com/developers/risk-management/3d-secure).

### Cancel a payment authorisation

> Cancels the authorisation hold on a payment, returning a unique reference for this request. You can cancel payments after authorisation only for payment methods that support distinct authorisations and captures.<br/>
> <br/>
> For more information, refer to [Cancel](https://docs.adyen.com/developers/payment-modifications#cancel).

### Cancel or refund a payment

> Cancels a payment if it has not yet been captured yet, or refunds it if it has already been captured. This is useful when it is not certain if the payment has been captured or not (for example, when using auto-capture).<br/>
> <br/>
> For more information, refer to [Cancel or refund](https://docs.adyen.com/developers/payment-modifications#cancelorrefund).

### Capture a payment authorisation

> Captures the authorisation hold on a payment, returning a unique reference for this request. Usually the full authorisation amount is captured, however it's also possible to capture a smaller amount, which results in cancelling the remaining authorisation balance.<br/>
> <br/>
> Payment methods, which automatically capture as part of authorisation, don't need to be captured, but submitting a capture request on these transactions will not result in double charges. If immediate or delayed auto-capture is enabled, calling the capture method is not neccessary.<br/>
> <br/>
> For more information, refer to [Capture](https://docs.adyen.com/developers/payment-modifications#capture).

### Refund a payment

> Refunds a payment that has previously been captured, returning a unique reference for this request. Refunding can be done on the full captured amount or a partial amount. Multiple (partial) refunds will be accepted as long as their sum doesn't exceed the captured amount. Payments which have been authorised, but not captured, cannot be refunded, use the /cancel method instead.<br/>
> <br/>
> > Some payment methods/gateways do not support partial/multiple refunds.<br/>
> > A margin above the captured limit can be configured to cover shipping/handling costs.<br/>
> <br/>
> For more information, refer to [Refund](https://docs.adyen.com/developers/payment-modifications#refund).

## License

**flow**ground :- Telekom iPaaS / adyen-com-payment-service-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.

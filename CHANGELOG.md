# Changelog

## 1.11.0 - 2023-03-24
- Rename collections
- Fix an bug that if the timestamp is not in the last second position, the request could return error.

## 1.10.0 - 2022-12-23
### Spot API Collection
#### Added
VIP Loans:
- `GET /sapi/v1/loan/vip/collateral/account`: Check Locked Value of VIP Collateral Account
- `GET /sapi/v1/loan/vip/ongoing/orders`: Get VIP Loan Ongoing

Orders
- `POST /sapi/v1/loan/vip/repay`: VIP Loan Repay
- `GET /sapi/v1/loan/vip/repay/history`: Get VIP Loan Repayment History

Crypto Loan:
- `GET /sapi/v1/loan/loanable/data`: Get interest rate and borrow limit of loanable assets. The borrow limit is shown in USD value.
- `GET /sapi/v1/loan/collateral/data`: Get LTV information and collateral limit of collateral assets. The collateral limit is shown in USD value.
- `GET /sapi/v1/loan/repay/collateral/rate`: Get the the rate of collateral coin / loan coin when using collateral repay, the rate will be valid within 8 second.
- `POST /sapi/v1/loan/customize/margin_call`: Customize margin call for ongoing orders only.

Convert:
- `GET /sapi/v1/convert/exchangeInfo`: Query for all convertible token pairs and the tokens’ respective upper/lower limits
- `GET /sapi/v1/convert/assetInfo`: Query for supported asset’s precision information
- `POST /sapi/v1/convert/getQuote`: Request a quote for the requested token pairs
- `POST /sapi/v1/convert/acceptQuote`: Accept the offered quote by quote ID.
- `GET /sapi/v1/convert/orderStatus`: Query order status by order ID.

Wallet:
- `POST /sapi/v1/asset/convert-transfer`: New parameter accountType
- `POST /sapi/v1/asset/convert-transfer/queryByPage`: request method is changed to GET, new parameter clientTranId
- `GET /sapi/v1/asset/ledger-transfer/cloud-mining/queryByPage`: The query of Cloud-Mining payment and refund history
Sub-account:
- `GET /sapi/v1/sub-account/apiRestrictions/ipRestriction/thirdPartyList`: To query Sub-Account API key Third Party IP whitelist
- `POST /sapi/v2/sub-account/subAccountApi/ipRestriction`: To support master account update IP Restriction for Sub-Account API key

Binance Code:
- `POST /sapi/v1/giftcard/buyCode`: For buying a fixed-value Binance Code.
- `GET /sapi/v1/giftcard/buyCode/token-limit`: To verify which tokens are available for you to purchase fixed-value gift cards as mentioned in section 2 and its’ limitation.
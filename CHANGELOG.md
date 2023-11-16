# Changelog


## 1.13.0 -2023-11-16

#### Update
- `GET /dapi/v1/income` Add parameter `page` for pagination
- `GET /fapi/v1/income` Add parameter page for pagination
- Add optional parameter `goodTillDate` in the endpoints below to set order's goodTillDate :
	- `POST /fapi/v1/order`
- Add optional parameter `priceMatc`h in the endpoints below to set order's priceMatch mode:
	- `POST /fapi/v1/order`
- Add optional parameter `selfTradePreventionMode` in the endpoints below to set order's STP mode:
	- `POST /fapi/v1/order`
- `POST /sapi/v1/loan/vip/borrow` add field isFlexibleRate to borrow using flexible rate loan
- `POST /sapi/v1/simple-earn/flexible/subscribe` new parameter sourceAccount
- `POST /sapi/v1/simple-earn/locked/subscribe` new parameter sourceAccount
- `POST /sapi/v1/simple-earn/flexible/redeem` new parameter destAccount
- Changes to Margin Endpoint `GET /sapi/v1/margin/isolated/transfer`:
	- Add request field `type`
	- Delete request field `transFrom`, `transTo`
- `POST /sapi/v1/portfolio/repay` add paramater from

#### Add
- `GET /dapi/v1/income/asyn` get Download Id For Futures Transaction History
- `GET /dapi/v1/income/asyn/id` to get Futures Transaction History Download Link by Id
- `GET /dapi/v1/fundingInfo` query adjusted funding info
- `GET /dapi/v1/constituents` query index constituents
- `GET /futures/data/delivery-price` query quarterly contract settlement price
- `GET /fapi/v1/fundingInfo` query adjusted funding info
- `GET /fapi/v1/constituents` query index constituents
- `GET /futures/data/delivery-price` query quarterly contract settlement price
- `GET /futures/data/basis` query basis data
- New endpoints for order placement using SOR:
	- `POST /api/v3/sor/order`
	- `POST /api/v3/sor/order/test`
- `GET /api/v3/myAllocations`
- `POST /sapi/v1/loan/flexible/borrow` flexible Loan borrow
- `GET /sapi/v1/loan/flexible/ongoing/orders` get flexible loan ongoing orders
- `GET /sapi/v1/loan/flexible/borrow/history` Get flexible loan borrow history
- `POST /sapi/v1/loan/flexible/repay` flexible loan repay
- `POST /sapi/v1/loan/flexible/repay/history` Get flexible loan repayment history
- `POST /sapi/v1/loan/flexible/adjust/ltv` adjust flexible Loan adjust LTV
- `GET /sapi/v1/loan/flexible/ltv/adjustment/history` Get Flexible loan LTV adjustment history
- `GET /sapi/v1/loan/flexible/loanable/data` Get flexible loan assets data
- `GET /sapi/v1/loan/flexible/collateral/data` Get flexible loan collateral assets data
- `GET /sapi/v1/margin/capital-flow` Get cross or isolated margin capital flow
- `GET /sapi/v1/portfolio/margin-asset-leverage` Get Portfolio Margin Asset Leverage
- `GET /sapi/v1/lending/auto-invest/index/info` query index details
- `GET /sapi/v1/lending/auto-invest/index/user-summary` query index linked plan position details
- `POST /sapi/v1/lending/auto-invest/one-off` One Time transaction
- `GET /sapi/v1/lending/auto-invest/one-off/status` query one-time transaction status
- `POST /sapi/v1/lending/auto-invest/redeem` index linked plan redemption
- `GET /sapi/v1/lending/auto-invest/redeem/history` query index Linked plan Redemption history
- `GET /sapi/v1/lending/auto-invest/rebalance/history` query index linked plan rebalance details
- `GET /sapi/v1/asset/wallet/balance` query user wallet balance
- `GET /sapi/v1/asset/custody/transfer-history` query user delegation history(For Master Account)
- `GET /sapi/v1/futures/histDataLink` query futures ticklevel orderbook historicak data download link
- `GET /sapi/v1/loan/vip/request/interestRate` Get Borrow Interest Rate
- `GET /sapi/v1/margin/available-inventory` Query margin available inventory
- `POST /sapi/v1/margin/manual-liquidation` Margin manual liquidation

#### Delete
- `GET /sapi/v1/futures/loan/borrow/history`
- `GET /sapi/v1/futures/loan/repay/history`
- `GET /sapi/v2/futures/loan/wallet`
- `GET /sapi/v1/futures/loan/adjustCollateral/history`
- `GET /sapi/v1/futures/loan/liquidationHistory`
- `GET /sapi/v1/futures/loan/interestHistory`


## 1.12.0 - 2023-08-07

### Spot API Collection
#### Added
Spot Algo:
- `POST /sapi/v1/algo/spot/newOrderTwap`: Place a new spot TWAP order with Algo service.
- `DELETE /sapi/v1/algo/spot/order`: Cancel an open TWAP order.
- `GET /sapi/v1/algo/spot/openOrders`: Get all open SPOT TWAP orders.
- `GET /sapi/v1/algo/spot/historicalOrders`: Get all historical SPOT TWAP orders.
- `GET /sapi/v1/algo/spot/subOrders`: Get respective sub orders for a specified algoId.

Sub-Account:
- `GET /sapi/v1/managed-subaccount/deposit/address`: Get investor's managed sub-account deposit address.
- `GET /sapi/v1/managed-subaccount/query-trans-log`: Query Managed Sub Account Transfer Log (For Trading Team Sub Account).
- `GET /sapi/v1/managed-subaccount/queryTransLogForInvestor`: Investor can use this api to query managed sub account transfer log. This endpoint is available for investor of Managed Sub-Account. A Managed Sub-Account is an account type for investors who value flexibility in asset allocation and account application, while delegating trades to a professional trading team.
- `GET /sapi/v1/managed-subaccount/queryTransLogForTradeParent`: Trading team can use this api to query managed sub account transfer log.
- `GET /sapi/v1/managed-subaccount/fetch-future-asset`: Investor can use this api to query managed sub account futures asset details.
- `GET /sapi/v1/managed-subaccount/marginAsset`: Investor can use this api to query managed sub account margin asset details.
- `GET /sapi/v1/managed-subaccount/info`: Get investor's managed sub-account list.
- `POST /sapi/v1/sub-account/eoptions/enable`: Enable Options for Sub-account (For Master Account).
- `GET /sapi/v4/sub-account/assets`: Fetch sub-account assets
- `GET /sapi/v1/sub-account/transaction-statistics`: Query Sub-account Transaction statistics (For Master Account).

Portfolio:
- `GET /sapi/v1/portfolio/asset-index-price`: Query Portfolio Margin Asset Index Price.
- `GET /sapi/v1/portfolio/repay-futures-switch`: Change Auto-repay-futures Status.
- `POST /sapi/v1/portfolio/auto-collection`: Transfers all assets from Futures Account to Margin account.
- `POST /sapi/v1/portfolio/bnb-transfer`: BNB transfer can be between Margin Account and USDM Account.
- `POST /sapi/v1/portfolio/repay-futures-switch`: Change Auto-repay-futures Status.
- `POST /sapi/v1/portfolio/repay-futures-negative-balance`: Repay futures Negative Balance.
- `POST /sapi/v1/portfolio/asset-collection`: Transfers specific asset from Futures Account to Margin account.
- `GET /sapi/v1/portfolio/interest-history`: Query interest history of negative balance for portfolio margin.

Wallet:
- `POST /sapi/v1/capital/deposit/credit-apply`: Apply deposit credit for expired address (One click arrival).
- `GET /sapi/v1/capital/contract/convertible-coins`: Get a user's auto-conversion settings in deposit/withdrawal.
- `POST /sapi/v1/capital/contract/convertible-coins`: User can use it to turn on or turn off the BUSD auto-conversion from/to a specific stable coin.

Simple Earn:
- `GET /sapi/v1/simple-earn/flexible/list`: Get available Simple Earn flexible product list.
- `GET /sapi/v1/simple-earn/locked/list`: Get available Simple Earn locked product list.
- `POST /sapi/v1/simple-earn/flexible/subscribe`: Subscribe flexibe product.
- `POST /sapi/v1/simple-earn/locked/subscribe`: Subscribe locked product.
- `POST /sapi/v1/simple-earn/flexible/redeem`: Redeem flexible product.
- `POST /sapi/v1/simple-earn/locked/redeem`: Redeem locked product.
- `GET /sapi/v1/simple-earn/flexible/position`: Get flexible product position.
- `GET /sapi/v1/simple-earn/locked/position`: Get locked product position.
- `GET /sapi/v1/simple-earn/account`: Get account details.
- `GET /sapi/v1/simple-earn/flexible/history/subscriptionRecord`: Get flexible subscription record.
- `GET /sapi/v1/simple-earn/locked/history/subscriptionRecord`: Get locked subscription record.
- `GET /sapi/v1/simple-earn/flexible/history/redemptionRecord`: Get flexible redemption record.
- `GET /sapi/v1/simple-earn/locked/history/redemptionRecord`: Get locked redemption record.
- `GET /sapi/v1/simple-earn/flexible/history/rewardsRecord`: Get flexible rewards history.
- `GET /sapi/v1/simple-earn/locked/history/rewardsRecord`: Get locked rewards history.
- `POST /sapi/v1/simple-earn/flexible/setAutoSubscribe`: Set flexible auto subscribe.
- `POST /sapi/v1/simple-earn/locked/setAutoSubscribe`: Set locked auto subscribe.
- `GET /sapi/v1/simple-earn/flexible/personalLeftQuota`: Get flexible personal left quota.
- `GET /sapi/v1/simple-earn/locked/personalLeftQuota`: Get locked personal left quota.
- `GET /sapi/v1/simple-earn/flexible/subscriptionPreview`: Get flexible subscription preview.
- `GET /sapi/v1/simple-earn/locked/subscriptionPreview`: Get locked subscription preview.
- `GET /sapi/v1/simple-earn/flexible/history/rateHistory`: Get rate history.
- `GET /sapi/v1/simple-earn/flexible/history/collateralRecord`: Get collateral record.

Auto-Investment:
- `GET /sapi/v1/lending/auto-invest/target-asset/list`: Get target asset list.
- `GET /sapi/v1/lending/auto-invest/target-asset/roi/list`: ROI return list for target asset.
- `GET /sapi/v1/lending/auto-invest/all/asset`: Query all source assets and target assets.
- `GET /sapi/v1/lending/auto-invest/source-asset/list`: Query Source Asset to be used for investment.
- `GET /sapi/v1/lending/auto-invest/plan/list`: Query plan lists.
- `GET /sapi/v1/lending/auto-invest/plan/id`: Query holding details of the plan
- `GET /sapi/v1/lending/auto-invest/history/list`: Query subscription transaction history of a plan
- `POST /sapi/v1/lending/auto-invest/plan/add`: Post an investment plan creation.
- `POST /sapi/v1/lending/auto-invest/plan/edit`: Query Source Asset to be used for investment.
- `POST /sapi/v1/lending/auto-invest/plan/edit-status`: Change Plan Status.

Margin:
- `GET /sapi/v1/margin/dust`: Get assets that can be converted into BNB.
- `POST /sapi/v1/margin/dust`: Convert dust assets to BNB.
- `GET /sapi/v1/margin/crossMarginCollateralRatio`: Get cross margin account details.
- `GET /sapi/v1/margin/exchange-small-liability`: Query the coins which can be small liability exchange.
- `POST /sapi/v1/margin/exchange-small-liability`: Cross Margin Small Liability Exchange.
- `GET /sapi/v1/margin/exchange-small-liability-history`: Get Small liability Exchange History.
- `GET /sapi/v1/margin/next-hourly-interest-rate`: Get user the next hourly estimate interest.
- `GET /sapi/v1/margin/delist-schedule`: Get tokens or symbols delist schedule for cross margin and isolated margin.
- `POST /sapi/v1/margin/max-leverage`: Adjust cross margin max leverage

VIP loan:
- `POST /sapi/v1/loan/vip/renew`: VIP loan is available for VIP users only.
- `POST /sapi/v1/loan/vip/borrow`: VIP loan is available for VIP users only.
- `GET /sapi/v1/loan/vip/loanable/data`: Get interest rate and borrow limit of loanable assets. The borrow limit is shown in USD value.
- `GET /sapi/v1/loan/vip/collateral/data`: Get Collateral Asset Data.
- `GET /sapi/v1/loan/vip/request/data`: Query the application status.


#### Updated
Margin:
- `POST /sapi/v1/margin/order`: Add fields `autoRepayAtCancel` and `selfTradePreventionMode`:
- `POST /sapi/v1/margin/order/oco`: Add fields `autoRepayAtCancel` and `selfTradePreventionMode`


#### Deleted
Lending:
- `GET /sapi/v1/lending/daily/product/list`
- `GET /sapi/v1/lending/daily/userLeftQuota`
- `GET /sapi/v1/lending/daily/userRedemptionQuota`
- `GET /sapi/v1/lending/daily/token/position`
- `GET /sapi/v1/lending/union/account`
- `GET /sapi/v1/lending/union/purchaseRecord`
- `GET /sapi/v1/lending/union/redemptionRecord`
- `GET /sapi/v1/lending/union/interestHistory`
- `POST /sapi/v1/lending/daily/redeem`
- `POST /sapi/v1/lending/daily/purchase`

Sub-Account:
- `POST /sapi/v1/sub-account/subAccountApi/ipRestriction`
- `POST /sapi/v1/sub-account/subAccountApi/ipRestriction/ipList`


### USDⓈ-Margined Futures Collection
#### Added
- `PUT /fapi/v1/order`: Order modify function, currently only LIMIT order modification is supported, modified orders will be reordered in the match queue.
- `PUT /fapi/v1/batchOrders`: Modify Multiple Orders.
- `GET /fapi/v1/orderAmendment`: Get order modification history.
- `GET /fapi/v1/order/asyn`: Get download id for futures order history.
- `GET /fapi/v1/order/asyn/id`: Get futures order history download link by id.
- `GET /fapi/v1/trade/asyn`: Get download id for futures trade history.
- `GET /fapi/v1/trade/asyn/id`: Get futures trade download link by id.


#### Deleted
- `GET /fapi/v1/pmExchangeInfo`


### European Options Collection
#### Added
- `GET /eapi/v1/order`: Check an order status.
- `GET /eapi/v1/income/asyn/id`: Get option transaction history download link by id.
- `GET /eapi/v1/income/asyn`: Get download id for option transaction history.


#### Deleted
- `/eapi/v1/transfer`


## 1.11.1 - 2023-04-14
- Added missing X-MBX-APIKEY and Content Type headers to the Crypto Loan endpoints

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
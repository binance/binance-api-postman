# Postman collection environment

Binance now has serval Postman Collections for quick and easy exercise of our REST-based APIs. The environment hosted here can be imported for easy changing of API public key, secret key. Use the button below for easy import into Postman. 

|   Collections    |       Click to Run     |  Document |
| :--------------- | :---------------------------------- | :-----|
| Binance Spot API | [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/7c052414684953667296) | [https://binance-docs.github.io/apidocs/spot/en](https://binance-docs.github.io/apidocs/spot/en)
| Binance Futures API | [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/6eacab304784a36a8243) | [https://binance-docs.github.io/apidocs/futures/en](https://binance-docs.github.io/apidocs/futures/en)


## How to import environment
- Download the environment json file
- Click the `Run in Postman` button above to import collection
    
- Click the button `Manage Environments`(gear icon) from the top right of Postman console (Postman Mac version)
    <p align="center"><img src="https://raw.githubusercontent.com/Binance-docs/binance-api-postman-environment/assets/postman/1.png"/></p>
- From the pop-up page, click `import` button, then select the downloaded json file.Click the environment,
   <p align="center"><img src="https://raw.githubusercontent.com/Binance-docs/binance-api-postman-environment/assets/postman/2.png"/></p>
- Set the API key and secret key. Leave timestamp and signature empty.
    <p align="center"><img src="https://raw.githubusercontent.com/Binance-docs/binance-api-postman-environment/assets/postman/3.png"/></p>
    
- Select the environment from the dropdown.
    <p align="center"><img src="https://raw.githubusercontent.com/Binance-docs/binance-api-postman-environment/assets/postman/4.png"/></p>

## Q&A
### Error: `Could not get any response`
- Either you haven't setup the environment or the environment is not selected. Please find the step above to setup the environment.

### Error: `API-key format invalid.`
- API key is not set.
- API key is not correct.
- In Postman `Headers`, the `X-MBX-APIKEY` is not selected.

### Error: `Signature for this request is not valid.`
Serval reasons can cause this error:
- Secret key is not set.
- Parameters are selected, but didn't pass any value. Uncheck the parameter if you don't use it.

### Error: `Mandatory parameter 'xxxx' was not sent, was empty/null, or malformed.`
- The mandatory parameter is missing. Please refer to the API document and pass all required parameters.


## What is Postman
[Click here](https://www.getpostman.com/)

# Binance API Postman

[Postman](https://getpostman.com) is an API Collaboration Platform.

Binance now offers several Postman Collections for quick and easy usage of our RESTful APIs. <br>
We also provide a Postman environment (JSON configuration file), which can be conveniently imported for use with your own API and secret keys.

## How to import Collections

    
- Click the button `Manage Environments`(gear icon) from the top right of Postman console (Postman Mac version)
    <p align="center"><img src="https://raw.githubusercontent.com/binance-exchange/binance-api-postman/assets/postman/1.png"/></p>
- From the pop-up page, click `import` button, then select the downloaded json file.Click the environment,
   <p align="center"><img src="https://raw.githubusercontent.com/binance-exchange/binance-api-postman/assets/postman/2.png"/></p>
- Set the API key and secret key. Leave timestamp and signature empty.
    Please DON'T set into `INTIAL VALUE` column, otherwise postman will upload into your personal postman account. Don't leave `INTIAL VALUE` empty, postman can copy the `CURRENT VALUE` into here.
    <p align="center"><img src="https://raw.githubusercontent.com/binance-exchange/binance-api-postman/assets/postman/3.png"/></p>
- Download the Collections.
- Import the Collections into the Postman app.
## How to import the environment
- Download the environment JSON file.
- Open the Postman app.
    
- Select the environment from the dropdown.
    <p align="center"><img src="https://raw.githubusercontent.com/binance-exchange/binance-api-postman/assets/postman/4.png"/></p>

## Guide for using the Binance API with Postman

https://academy.binance.com/economics/binance-api-series-pt-1-spot-trading-with-postman

## FAQ
### Error: `Could not get any response`
- Either you haven't setup the environment or the environment is not selected. Please find the step above to setup the environment.

### Error: `API-key format invalid.`
- API key is not set.
- API key is not correct.
- In Postman `Headers`, the `X-MBX-APIKEY` is not selected.

### Error: `Signature for this request is not valid.`
These are the likely reasons that can cause this error:
- Secret key is not set.
- Parameters are selected, but didn't pass any value. Uncheck the parameter if you don't use it.

### Error: `Mandatory parameter 'xxxx' was not sent, was empty/null, or malformed.`
- The mandatory parameter is missing. Please refer to the API document and pass all required parameters.

### How to debug or find out request URL
- Open Postman console `(CMD/CTRL + ALT + C)`, each request will print request parameters and URL.
- Edit Pre-request scripts for debugging.

## Is Postman safe to use
We suggest users to develop their own application to work with Binance API. However Postman is a good tool for those who want to easily experience APIs. These best pratices are recommended:

- Don't use collections from distrust channel.
- Review the json file before using it.
- Don't use if any code that you don't understand.
- Make sure that withdrawals are not enabled on your API keys. 
- Delete API key after use. 

## My question isn't here
Please open an issue [here](https://github.com/binance-exchange/binance-api-postman/issues).

## License
MIT

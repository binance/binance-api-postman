[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# Binance API Postman

[Postman](https://getpostman.com) is an API Collaboration Platform.

Binance now offers several Postman Collections and Environments (JSON files) for a quicker and easier usage of our RESTful APIs.<br/>
You only need to import and set up with your own API and secret keys to begin.

## How to import and configure

- Download the `binance-api-postman` repository.

- Click the `Import` button. On Postman for Mac, for example, the button is at the top left:
    <p align="center"><img src="assets/1.png" alt="Screenshot of Postman for Mac, with 'Import' button pointed out at top left."/></p>

- On the `Import` pop-up page, select the root folder of the downloaded repository.
   <p align="center"><img src="assets/2.png" alt="Screenshot of of Postman for Mac, showing the Import screen."/></p>

- Select which collections and environments you would like to import and click the `Import` button.
   <p align="center"><img src="assets/3.png" alt="Screenshot of of Postman for Mac, showing the Import screen after selecting the folder."/></p>

- Select the `Environments` tab on the left, choose an environment, and set your API and Secret Key by changing the `Current Value` column (see screenshot);
    <p align="center"><img src="assets/4.png" alt="Screenshot of Postman for Mac, showing where the user should fill in their API and secret keys."/></p>

- Select your newly-added environment from the environment dropdown menu. On Mac, this is at top right, to the left of the eye icon.
    <p align="center"><img src="assets/5.png" alt="Screenshot of Postman for Mac, showing how imported environments can be selected from a dropdown ."/></p>

## Postman safety practices

The following practices are advised to secure your account's safety:

- Don't use Collections obtained from an unknown source.
- Review the environment JSON file before its usage.
- Don't use any code that you don't understand.
- Make sure that the withdrawal permission **is not enabled** for your API keys.
- When you finish trying out the API, delete your API keys.

## FAQ

**Q:** Why I can't get any response?

You haven't imported the environment file or you've imported it but haven't selected it from the dropdown menu (mentioned in [[How to import and configure]])

**Q:** How can I debug a request or find the used URL?

- Open the Postman's console to find requests' parameters and URL.
- Debugging can be done by editing the `Pre-request Script` tab.

**Q:** Error `API-key format invalid.`

Likely causes:

- API key is not set.
- API key is not correct.
- `X-MBX-APIKEY` is not selected in your Postman `Headers` tab.

**Q:** Error `Signature for this request is not valid.`

Likely causes:

- Secret key is not set.
- Request was made with at least one empty parameter.
- `signature` is not the last parameter in the parameters list.

**Q:** Error `Mandatory parameter 'xxxx' was not sent, was empty/null, or malformed.`

Please refer to the API documentation to double check all the mandatory parameters.

## My question isn't here

If you don't find your answer here, please consult <https://dev.binance.vision/> for similar questions from the community or
open an issue [here](https://github.com/binance/binance-api-postman/issues).

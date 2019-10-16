# Add an animated typing indicator to your Vue chat app Using CometChat PRO

This sample app shows how to build a group chat application with typing indicator using Vuejs and powered by CometChat Pro SDK

SCREENSHOTS

![Typing indicator 1](screenshots/screenshot_1.png)


## Running the demo locally

* Download the repository [here]() or run `git clone https://github.com/cometchat-pro-tutorials/vue-typing-indicators.git`
* In the `vue-typing-indicators` directory, run `npm install`
* You need to sign up for CometChat PRO and create your application first
* Create an ApiKey. You can use auth-only permission for this application
* Create a Group from the dashboard or use the group created by CometChat named `supergroup`
* Create a `.env` file in the root folder of the project and paste the following content in it:

```
VUE_APP_COMMETCHAT_API_KEY=YOUR_API_KEY                
VUE_APP_COMMETCHAT_APP_ID=YOUR_APP_ID
VUE_APP_COMMETCHAT_GUID=YOUR_GROUP_GUID
```

Replace `YOUR_API_KEY`, `YOUR_APP_ID` and `YOUR_GROUP_GUID` with your API KEY, APP ID and GUID as obtained from your CometChat dashboard.

* run `npm start`


## Technology

This demo uses:

* Vuejs
* CometChat Pro JavaScript SDK


## Useful links

* [📚Tutorial](https://prodocs.cometchat.com/docs)
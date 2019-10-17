<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import { CometChat } from "@cometchat-pro/chat";

import "./App.css";

export default {
  data() {
    return {
      username: ''
    }
  },
  created() {
    this.initializeApp();
    const username = prompt(`Welcome to our little Vue demo powered by CometChat. Login with the username superhero1 or superhero2 and test the chat out. To create your own user, copy this link 'https://prodocs.cometchat.com/reference#createuser' and paste into your address-bar`);
    this.authLoginUser(username);
  },

  methods: {
    initializeApp() {
      const { VUE_APP_COMMETCHAT_APP_ID } = process.env
      CometChat.init(VUE_APP_COMMETCHAT_APP_ID).then(
        () => {
          console.log("Initialization completed successfully");
        },
        error => {
          console.log("Initialization failed with error:", error);
        }
      );
    },
    authLoginUser(username) {
      var apiKey = process.env.VUE_APP_COMMETCHAT_API_KEY;

      CometChat.login(username, apiKey).then(
        () => {
          this.showSpinner = false;
          this.$router.push({
            name: "chat"
          });
        },
        error => {
          this.showSpinner = false;
          alert("Whops. Something went wrong. This commonly happens when you enter a username that doesn't exist. Check the console for more information")
          console.log("Login failed with error:", error.code);
        }
      );
    }
  }
};
</script>

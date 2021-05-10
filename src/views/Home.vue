<template>
  <div class="home">
    <!-- Messenger Wtyczka czatu Code -->
    <div id="fb-root"></div>
    <script>
      window.fbAsyncInit = function () {
        FB.init({
          xfbml: true,
          version: "v10.0",
        });
      };

      (function (d, s, id) {
        var js,
          fjs = d.getElementsByTagName(s)[0];
        if (d.getElementById(id)) return;
        js = d.createElement(s);
        js.id = id;
        js.src = "https://connect.facebook.net/pl_PL/sdk/xfbml.customerchat.js";
        fjs.parentNode.insertBefore(js, fjs);
      })(document, "script", "facebook-jssdk");
    </script>

    <!-- Your Wtyczka czatu code -->
    <div
      class="fb-customerchat"
      attribution="biz_inbox"
      page_id="106327708298802"
    ></div>
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src

export default defineComponent({
  name: "Home",
  components: {
    HelloWorld,
  },
});
</script>

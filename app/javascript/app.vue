<template>
  <div id="app">
    <v-app>
      <v-sheet
        height="100%"
        class="overflow-hidden"
        style="position: relative;">
      </v-sheet>
    </v-app>
  </div>
</template>

<script>

  export default {
    data: function () {
      return {
        showWriteInDialog: false,
        message: "Hello Vue!",
        items: [
          {title: 'Home', icon: 'mdi-home-city'},
          {title: 'My Account', icon: 'mdi-account'},
          {title: 'Users', icon: 'mdi-account-group-outline'},
        ],
      };
    },
    components: {
      WriteIn: WriteIn,
      'socials-menu': SocialsMenu,
      'TopMenu': TopMenu,
    }
  };
</script>

<style scoped>
  p {
    font-size: 2em;
    text-align: center;
  }
</style>

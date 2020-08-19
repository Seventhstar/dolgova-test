<template>
  <div id="app">
    <v-app>
      <v-sheet
<!--        height="100%"-->
<!--        class="overflow-hidden"-->
<!--        style="position: relative;">-->
<!--&lt;!&ndash;        <TopMenu/>&ndash;&gt;-->
<!--        <v-main>-->
<!--&lt;!&ndash;          <router-view></router-view>&ndash;&gt;-->
<!--          <socials-menu></socials-menu>-->
<!--        </v-main>-->
      </v-sheet>
<!--      <WriteIn></WriteIn>-->
    </v-app>
  </div>
</template>

<script>
  import TopMenu from "./packs/components/TopMenu.vue";
  import SocialsMenu from "./packs/components/SocialsMenu.vue";
  import WriteIn from "./packs/components/WriteIn";

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

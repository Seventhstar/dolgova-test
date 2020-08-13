<template>
  <div id="app">
    <v-app>
      <TopMenu/>
      <!--      <v-fab-transition>-->
      <!--        <v-btn color="red" dark top right>-->
      <!--          <v-icon>edit</v-icon>-->
      <!--          Записаться-->
      <!--        </v-btn>-->
      <!--      </v-fab-transition>-->
      <!--      <v-card>-->
      <!--        <v-navigation-drawer></v-navigation-drawer>-->
      <!--      </v-card>-->
      <v-sheet
        height="100%"
        class="overflow-hidden"
        style="position: relative;"
      >
        <v-main>
          <router-view></router-view>
        </v-main>
        <!--      <socials-menu></socials-menu>-->
        <div class="write-in">
          <v-fab-transition>
            <v-btn rounded color="red" key="edit" dark @click.stop="drawer = !drawer">
              <v-icon class="mr-2">edit</v-icon> Записаться
            </v-btn>
          </v-fab-transition>
        </div>


        <v-navigation-drawer class="ma-10"
                             v-model="drawer"
                             height="80%"
                             width="95%"

                             absolute
                             right
                             temporary
        >
          <v-list-item>
            <v-list-item-avatar>
              <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
            </v-list-item-avatar>
            <v-list-item-content>
              <v-list-item-title>Записаться на прием</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-divider></v-divider>
          <div class="d-flex flex-no-wrap justify-space-between">
            <v-list-item-content>
              <v-calendar></v-calendar>
            </v-list-item-content>
            <v-list-item-content aria-rowindex="1">

              <v-list>
                <v-list-item-content>
                  <v-list-item-title>John Leider</v-list-item-title>
                </v-list-item-content>
                <v-list-item>
                  <v-list-item-action>
                    <v-switch v-model="message" color="purple"></v-switch>
                  </v-list-item-action>
                  <v-list-item-title>Семейная</v-list-item-title>
                </v-list-item>
                <v-list-item>
                  <v-list-item-action>
                    <v-switch v-model="message" color="purple"></v-switch>
                  </v-list-item-action>
                  <v-list-item-title>Онлайн</v-list-item-title>
                </v-list-item>
              </v-list>

            </v-list-item-content>
          </div>


        </v-navigation-drawer>
      </v-sheet>

    </v-app>

  </div>
</template>

<script>
  import SocialsMenu from "./packs/components/SocialsMenu.vue";
  import TopMenu from "./packs/components/TopMenu.vue";

  export default {
    data: function () {
      return {
        message: "Hello Vue!",
        drawer: false
      };
    },
    components: {
      'TopMenu': TopMenu,
      'socials-menu': SocialsMenu,

    }
  };
</script>

<style scoped>
  p {
    font-size: 2em;
    text-align: center;
  }
</style>

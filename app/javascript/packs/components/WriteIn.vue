<template>
  <div>
    <div class="write-in">
      <v-fab-transition>
        <v-btn rounded color="red" key="edit" dark @click.stop="showWriteInDialog = !showWriteInDialog">
          <v-icon class="mr-2">edit</v-icon>
          Записаться
        </v-btn>
      </v-fab-transition>
    </div>


    <v-navigation-drawer class="ma-10 write-in-card"
                         v-model="showWriteInDialog"
                         height="80%"
                         width="95%"
                         absolute
                         right
                         temporary>
      <v-list-item class="write-in-header">
        <v-list-item-content dark>
          <v-list-item-title class="write-in-title">Записаться на прием</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <div class="d-flex flex-no-wrap justify-space-between">
        <v-list-item-content>
          <v-calendar></v-calendar>
        </v-list-item-content>

        <v-list-item-content aria-rowindex="1" class="ml-8" top>
          <v-list>
            <v-list-item-content>
              <v-list-item-title>Формат консультации</v-list-item-title>
            </v-list-item-content>
            <v-list-item>
              <v-list-item-action>
                <v-switch v-model="isGroup" color="purple"></v-switch>
              </v-list-item-action>
              <v-list-item-title>Семейная</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-action>
                <v-switch v-model="isOnline" color="purple"></v-switch>
              </v-list-item-action>
              <v-list-item-title>Онлайн</v-list-item-title>
            </v-list-item>
          </v-list>

        </v-list-item-content>
      </div>
    </v-navigation-drawer>

  </div>
</template>
<script>
  export default {
    name: 'WiteIn',
    data: function () {
      return {
        showWriteInDialog: false,
        isGroup: false,
        isOnline: false,
      }
    },
  }
</script>
<style>
  .write-in-header {
    background-color: #ddb8cb;
  }
  .write-in-card {
    border-radius: 5px
  }
  .write-in-title {
    text-align: center;
    align-items: center;
    color: white;
    font-size: 24px;
    font-family: roboto;
  }

</style>
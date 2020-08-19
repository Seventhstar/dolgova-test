<template>
  <div class="social-menu-container">
    <v-card>
      <v-navigation-drawer floating permanent expand-on-hover>
        <v-list>
          <v-list-item class="px-2">
            <v-list-item-avatar>
              <v-img :src="require('images/logo.jpg')"></v-img>
            </v-list-item-avatar>
            <!--            <v-list-item-content>-->
            <v-list-item-title class="title">Связаться со мной</v-list-item-title>
            <!--            </v-list-item-content>-->
          </v-list-item>
        </v-list>
        <v-divider/>
        <v-list nav dense>

          <v-list-item :href="item.link" v-for="item in items" :key="item.label" target="_blank">
            <v-list-item-icon>
              <img :src="require(`images/${item.icon}`)">
            </v-list-item-icon>
            <v-list-item-title>{{item.label}}</v-list-item-title>
          </v-list-item>

        </v-list>
      </v-navigation-drawer>
    </v-card>
  </div>
</template>

<script>
  export default {
    name: "SocialsMenu",
    data() {
      return {
        items: [
          {icon: 'vk24.png', label: 'В контакте', link: 'https://vk.com/id3598181'},
          {icon: 'insta24.png', label: '@psyholog.dolgova', link: 'https://www.instagram.com/psyholog.dolgova/'},
          {icon: 'telegram.png', label: 'Телеграм', link: ''},
          {icon: 'fb.png', label: 'facebook', link: ''},
          {icon: 'email.png', label: 'Написать письмо', link: 'mailto:seventhstar@mail.ru'},

        ]
      }
    },
  };
</script>
<style>
  .social-menu-container {
    position: absolute;
    display: flex;
    width: fit-content;
    top: 80px;
  }

  .social-menu-container .v-list--nav {
    /*padding-left: 0;*/
    /*padding-right: 0;*/
  }

  .social-menu-container .v-list-item {
    padding: 0 6px;
  }

  .social-menu-container .v-list-item__icon {
    height: 32px;
  }

  .social-menu-container .title {
    font-size: 16px !important;
  }

</style>

<!--<template>-->
<!--  <div>-->
<!--    <v-app-bar app dark color="pink lighten-4">-->

<!--      <div class="header">-->
<!--        <div class="h1">{{ appTitle }}</div>-->
<!--        <div class="h2"> {{ appSubTitle }}</div>-->
<!--      </div>-->


<!--      <v-spacer></v-spacer>-->
<!--      <v-icon></v-icon>-->
<!--      <v-toolbar-items class="hidden-xs-only">-->
<!--        <v-btn text replace-->
<!--               v-for="item in menuItems"-->
<!--               :key="item.title"-->
<!--               :to="item.path">-->
<!--          {{ item.title }}-->
<!--        </v-btn>-->

<!--      </v-toolbar-items>-->
<!--      <v-btn icon>-->
<!--        <v-icon>login</v-icon>-->
<!--      </v-btn>-->

<!--&lt;!&ndash;            <v-spacer></v-spacer>&ndash;&gt;-->
<!--&lt;!&ndash;            <v-toolbar-items class="hidden-xs-only">&ndash;&gt;-->
<!--&lt;!&ndash;              <v-btn&ndash;&gt;-->
<!--&lt;!&ndash;                      text&ndash;&gt;-->
<!--&lt;!&ndash;                      v-for="item in rightMenus"&ndash;&gt;-->
<!--&lt;!&ndash;                      :key="item.title"&ndash;&gt;-->
<!--&lt;!&ndash;                      :href="item.path">&ndash;&gt;-->
<!--&lt;!&ndash;                <v-icon left dark>{{ item.icon }}</v-icon>&ndash;&gt;-->
<!--&lt;!&ndash;                {{ item.title }}&ndash;&gt;-->
<!--&lt;!&ndash;              </v-btn>&ndash;&gt;-->
<!--&lt;!&ndash;            </v-toolbar-items>&ndash;&gt;-->

<!--    </v-app-bar>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--  export default {-->
<!--    name: "TopMenu",-->
<!--    data() {-->
<!--      return {-->
<!--        appTitle: 'Анастасия Долгова',-->
<!--        appSubTitle: 'Психолог',-->
<!--        sidebar: false,-->
<!--        rightMenus: [-->
<!--          {title: 'Sign Up', path: '/signup', icon: 'face'},-->
<!--          {title: 'Sign In', path: '/signin', icon: 'lock_open'}-->
<!--        ],-->
<!--        menuItems: [-->
<!--          {title: 'Обо мне', path: '/'},-->
<!--          {title: 'Блог', path: '/posts'},-->
<!--          {title: 'Контакты', path: '/statements'},-->
<!--        ],-->
<!--        fab: false,-->
<!--        hidden: false,-->
<!--        tabs: null,-->
<!--      }-->
<!--    },-->
<!--    computed: {-->
<!--      activeFab() {-->
<!--        switch (this.tabs) {-->
<!--          case 'one':-->
<!--            return {color: 'success', icon: 'share'}-->
<!--          case 'two':-->
<!--            return {color: 'red', icon: 'edit'}-->
<!--          case 'three':-->
<!--            return {color: 'green', icon: 'keyboard_arrow_up'}-->
<!--          default:-->
<!--            return {}-->
<!--        }-->
<!--      },-->
<!--    }-->
<!--  };-->
<!--</script>-->
<!--<style>-->

<!--</style>-->

<template>
 <div class="app-bar">
    <v-app-bar
      color="#474069"
      dense
      dark
      height="90"
    >
      <v-toolbar-title><v-img
  max-height="48"
  max-width="100"
  src="https://britg.kr/wp-content/themes/britg/img/gnb-logo.png?ver=0619"
></v-img></v-toolbar-title>

      <v-spacer></v-spacer>

     <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
          >
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="(item,n) in items"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
  </div>
</template>

<script>
    export default {
        name:'AppBar',
        data: () => ({
      items: [
        {
          icon: 'mdi-login',
          text: '로그인',
        },
        {
          icon: 'mdi-star',
          text: '회원가입',
        },
        {
          icon: 'mdi-account ',
          text: '마이페이지',
        }
      ],
      model: 1,
    }),
    }
</script>

<style lang="scss" scoped>
</style>
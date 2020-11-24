<template>
 <div class="app-bar">
    <v-app-bar
      color="#474069"
      dense
      dark
      height="60"
    >
      <v-toolbar-title><router-link to="/"> 
        <v-img
    :src="require('../../assets/logo.png')" alt="logo" contain
  ></v-img>
      </router-link></v-toolbar-title>

    
        <router-link to="/gnbmenu" class="menu">작품</router-link>
        <router-link to="/gnbmenu" class="menu">리뷰</router-link>
        <router-link to="/gnbmenu" class="menu">문학상</router-link>
        <router-link to="/gnbmenu" class="menu">프로젝트</router-link>
        <router-link to="/gnbmenu" class="menu">이벤트&커뮤니티</router-link>
        <router-link to="/gnbmenu" class="menu shop">SHOP</router-link>


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

    .menu{
      display: inline-block;
      font-size: 20px;
      color: #fff;
      padding-left: 80px;
    }


    .shop{
      position: relative;
      &:after{
        position: absolute;
        top: 0;
        right: -35px;
        content: '';
        display: block;
        width: 30px;
        height: 30px;
        background: url('https://britg.kr/wp-content/themes/britg/img/coin-gnb-icon.png') no-repeat 0 0;
      }
    }
</style>
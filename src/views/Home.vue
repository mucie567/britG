<template>
  <div class="home">
    <core-app-bar></core-app-bar>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: "Home",
  components: {
     CoreAppBar: () => import("@/components/core/AppBar.vue")
  }
};
</script>

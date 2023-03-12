<template>
  <the-header></the-header>
  <router-view v-if="isLoggedIn"></router-view>
</template>

<script>
import TheHeader from './components/nav/TheHeader.vue';

export default {
  components: {
    TheHeader
  },
  computed:{
    isLoggedIn(){
    return this.$store.getters.isLoggedIn;
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>
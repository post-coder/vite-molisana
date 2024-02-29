<script>
import AppNav from './components/AppNav.vue';
import AppProducts from './components/AppProducts.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppNav,
    AppProducts,
    AppFooter
  }
}
</script>

<template>
  <AppNav></AppNav>

  <AppProducts></AppProducts>

  <AppFooter></AppFooter>
</template>

<style lang="scss">

@use './styles/general' as *;

</style>
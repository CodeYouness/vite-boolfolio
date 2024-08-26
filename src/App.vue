<script>
import MainHeader from './components/MainHeader.vue';
import MainFooter from './components/MainFooter.vue';
export default {
  name: "",
  components: {
    MainHeader,
    MainFooter
  }
}
</script>

<template>
  <MainHeader/>
  <RouterView></RouterView>
  <MainFooter/>
</template>

<style lang="scss">
@use "./styles/partials/variable";
  @use "./styles/general.scss";
</style>

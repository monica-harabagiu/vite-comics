<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import FooterTop from './components/FooterTop.vue';
import '@fontsource/pt-sans-narrow';

export default {
  components: {
    AppHeader,
    AppMain,
    FooterTop
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <FooterTop />
</template>

<style lang="scss">
@use './style/general.scss' as *;
</style>

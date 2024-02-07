<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import FooterTop from './components/FooterTop.vue';
import FooterMain from './components/FooterMain.vue'
import '@fontsource/pt-sans-narrow';

export default {
  components: {
    AppHeader,
    AppMain,
    FooterTop,
    FooterMain
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <FooterTop />
  <FooterMain/>
</template>

<style lang="scss">
@use './style/general.scss' as *;
</style>

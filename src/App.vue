<script>
import AppHeader from './components/AppHeader.vue';
import MainContent from './components/MainContent.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  data() {
    return {

    }
  },
  components: {
    AppHeader,
    MainContent,
    AppFooter
  }
}
</script>

<template>
  <AppHeader />
  <MainContent />
  <AppFooter />
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
<template>
  <div id="app">
    <Header/>
    <MainItem/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import MainItem from './components/MainItem.vue';

export default {

  name: 'App',
  components: {
    Header,
    MainItem
  }
}
</script>

<style lang="scss">
@import '@/style/common.scss';
</style>
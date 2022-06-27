<template>
  <div id="app">
    <AlbumsList />
  </div>
</template>

<script>
import AlbumsList from './components/AlbumsList.vue';

export default {
  name: 'App',
  components: {
    AlbumsList,
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}
</style>

<template>
  <div class="card">
    <img class="card-img-top" :src="album.poster" :alt="`${album.title} cover`">
    <div class="card-body">
      <h5 class="card-title text-light text-uppercase">{{ album.title }}</h5>
      <h6 class="card-subtitle text-secondary">{{ album.author }}</h6>
      <h6 class="card-subtitle text-secondary">{{ album.year }}</h6>
    </div>
  </div>
</template>

<script>
export default {
  name: "AlbumData",
  props: {
    album: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.card {
  height: 100%;
  padding: 1.5rem;
  background-color: rgb(38, 49, 59);
  
    img {
      width: 100%;
      aspect-ratio: 1 / 1;
  }
}
</style>
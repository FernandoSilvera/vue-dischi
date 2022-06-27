<template>
  <div>
    <div class="card">
      <img :src="album.poster" :alt="`${album.title} cover`">
      <div class="card-body">
        <h5 class="card-title text-light">{{ album.title }}</h5>
        <h6 class="card-subtitle text-secondary">{{ album.author }}</h6>
        <h6 class="card-subtitle text-secondary">{{ album.year }}</h6>
      </div>
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
  background-color: rgb(38, 49, 59);
  
    img {
    object-fit: cover;
  }
}
</style>
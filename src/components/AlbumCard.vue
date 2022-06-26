<template>
  <div>
    <div class="card">
      <img :src="album.cover" :alt="`${album.title} cover`">
      <div class="card-body">
        <h5 class="card-title">{{ album.title }}</h5>
        <h6 class="card-subtitle">{{ album.author }}</h6>
        <h6 class="card-subtitle">{{ album.year }}</h6>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AlbumCard",
  props: {
    album: Object,
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
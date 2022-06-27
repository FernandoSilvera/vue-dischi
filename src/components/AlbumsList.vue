<template>
  <section>
    <div class="container">
      <div class="row row-cols-5">
        <div class="col" v-for="(album, i) in albumsList" :key="i">
          <AlbumData :album="album"></AlbumData>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from "axios";
import AlbumData from "./AlbumData.vue";

export default {
  name: "AlbumsList",
  components: { AlbumData },
  data() {
    return {
      urlAlbums: "https://flynn.boolean.careers/exercises/api/array/music",
      albumsList: [],
    }
  },
  methods: {
    fetchAlbumsData() {
      axios
      .get(this.urlAlbums)
      .then((resp) => {
        console.log(resp.data);
        this.albumsList = resp.data.response;
      })
    }
  },
  mounted() {
    this.fetchAlbumsData();
  },

}
</script>

<style>

</style>
<template>
  <div class="container mt-4">
      <div class="row flex-wrap w-100">
            <Album v-for="(album, index) in arrayAlbum" :key="index" :album="album" />          
          
        </div>
  </div>
</template>

<script>
import axios from "axios";
import Album from "../commons/Album.vue";

export default {
    name: 'AlbumsList',
    components: {
        Album
    },

    data(){
        return {
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
            arrayAlbum: [],
        }
    },
    created(){
        this.getAlbum();
    },
    methods: {
        getAlbum() {
        axios
            .get(this.apiURL)
            .then((risposta) => {
                 this.arrayAlbum = risposta.data.response;
          
             })
            .catch(function (error) {
                console.log(error);
            });
        },
    }
};
</script>

<style scoped lang="scss">

</style>
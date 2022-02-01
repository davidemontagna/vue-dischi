<template>
  <div class="container mt-4">
      
        <div v-if="!loading" class="row flex-wrap w-100">
          
            <Album v-for="(album, index) in arrayAlbum" :key="index" :album="album" />          
          
        </div>
        <Loader v-else />
  </div>
</template>

<script>
import axios from "axios";
import Album from "../commons/Album.vue";
import Loader from "../commons/Loader.vue";

export default {
    name: 'AlbumsList',
    components: {
        Album,
        Loader
    },

    data(){
        return {
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
            arrayAlbum: [],
            loading: true,
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
                this.loading = false;
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
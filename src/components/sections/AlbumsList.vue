<template>
    <div class="container mt-4">
        
        <div v-if="!loading" class="row flex-wrap w-100">
            <div>
                <Search @filter="filtrated"/>
            </div>
            <Album 
            v-for="(album, index) in filterAlbums"
            :key="index"
            :album="album" />          
            
        </div>

        <Loader v-else />
    </div>
</template>

<script>
import axios from "axios";
import Album from "../commons/Album.vue";
import Loader from "../commons/Loader.vue";
import Search from '../commons/Search.vue';

export default {
    name: 'AlbumsList',
    components: {
        Album,
        Loader,
        Search
    },

    data(){
        return {
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
            arrayAlbum: [],
            loading: true,
            newSearch: "",
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

        filtrated(album){
            this.newSearch = album
            console.log(this.newSearch)
        }
    },

    computed: {
        filterAlbums(){
            if(this.newSearch == ""){
                return this.arrayAlbum
            }
            return this.arrayAlbum.filter((album) =>{
                return album.genre.includes(this.newSearch)
            })
        }
    }
};
</script>

<style scoped lang="scss">

</style>
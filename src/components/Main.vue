<template>
  <main>
        <div class="container">
            <div class="row">
                <div class="col-12 col-sm-6 col-lg-3 w-100">
                    <AlbumsList />
            </div>
        </div>
    </div>     

  </main>
</template>

<script>
import AlbumsList from "./sections/AlbumsList.vue";

export default {
    name: 'Main',
    components:{
        AlbumsList
    }
}
</script>

<style scoped lang="scss">
@import '../assets/style/global.scss';

 main{
     background-color: $dm-bg-main;     
 }
</style>
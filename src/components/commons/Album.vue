<template>
  <div class="album mx-3 mb-4 justify-content-center text-center">
      <img :src="album.poster" alt="">
      <h3 class="my-3">{{album.title}}</h3>
      <h4 class="mt-4">
          {{album.author}} <br>
          {{album.year}}
      </h4>
  </div>
</template>

<script>
export default {
    name: 'Album',
    props: {
        album: Object,
    },
};
</script>

<style scoped lang="scss">

.album{
    @import '../../assets/style/global.scss';
    
    background-color: $dm-bg-album;
    width: 210px;
    text-align: center;
    padding: 15px;
    

    img{
        height: 170px;
        width: 100%;
        
    }
    h3{
        color: $titles-color;
        text-transform: uppercase;
    }
    h4{
        color: $text-color;
        
    }
    
}

</style>
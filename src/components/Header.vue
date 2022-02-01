<template>
  <header>
      <div class="bg-logo">
          <img src="https://upload.wikimedia.org/wikipedia/commons/7/71/Spotify.png" alt="">
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped lang="scss">
    .bg-logo{
        padding: 10px;        
        width: 100%;
        background-color: #2e3a46;

        img{
            
            height: 45px;
        }
    }
</style>
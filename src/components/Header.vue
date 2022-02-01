<template>
  <header>
      <div class="container dm-bg-header-color">
            <div class="row">
                <div class="col">
                    <div class="bg-logo justify-content-start">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/7/71/Spotify.png" alt="">
                        
                        
                     </div>
                </div>
            </div>
      </div>
      
  </header>
</template>

<script>


export default {
    name: 'Header',
    
}
</script>

<style scoped lang="scss">
    header{
        background-color: #2e3a46;
        width: 100%;
        padding: 10px; 
    }

    .bg-logo{           
        img{            
            height: 45px;
        }
    }

    
</style>
<template>
  <div class="header">
    <div class="logo">
      <img src="../assets/style/Spotify-png.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header{
  width:100%;
  background-color: rgb(49, 49, 66);
  img{
    width: 100px;
  }
}
</style>

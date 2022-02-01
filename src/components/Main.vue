<template>
  <div class="main">
    <Album/>
  </div>
</template>

<script>
import Album from "../sections/Album.vue"

export default {

  name: 'Main',
    components:{
      Album, 
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.main{
  width:100%;
  height: 100vh;
  height: calc(100vh - 104px);
  background-color: rgb(45, 45, 59);
}
</style>

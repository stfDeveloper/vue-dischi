<template>
  <div class="canzone">
      <img 
      :src="canzone.poster" 
      alt=""
      >
      <h5> 
          {{canzone.title}}
      </h5>
      <p class="text">{{canzone.author}} <br> 
      {{canzone.year}}
      </p>
  </div>
</template>

<script>
export default {
    name: "Musica",
    props: {
        canzone: Object,
    }
}
</script>

<style lang="scss">
.canzone{
    padding: 10px 5 px;
    width: 150px;
    height: 150px;
    text-align: center;
    img{
        width: 50%;
        height: 50%;
    }
    h5{
        color: black;
    }
    p{
        color: rgba(0, 0, 0, 0.829);
    }
}


</style>
<template>
  <div class="card">
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
.card{
    padding: 10px 10px;
    width: 180px;
    height: 220px;
    text-align: center;
    background-color: rgb(49, 49, 66);
    margin: 20px;

    img{
        width: 80%;
        height: 70%;
    }
    h5{
        color: black;
    }
    p{
        opacity: 0.4;
    }
}
</style>
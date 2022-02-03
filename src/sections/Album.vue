<template>
  <div class="container">
    <div>
        <Search @filter="filtrated"/>
    </div>
      <div class="canzone">
      <Musica v-for="(Musica, index) in musicaArray"
      :key="index"
      :canzone="Musica" 
      />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Musica from "./Musica.vue";
import Search from "./Search.vue";

export default {
    name:"Album",
    data(){
        return{
            apiURL:"https://flynn.boolean.careers/exercises/api/array/music",
            musicaArray:[],
            filterGenre:"",
        }
    },
    components: {
        Musica,
        Search,
    },
    created(){
        this.caricamentoMusica()
    },
    computed:{
        FilterAlbums(){
            if(this.filterGenre == ""){
                return this.musicaArray
            }
            return this.musicaArray.filter((canzone) =>{
                return canzone.genre.includes(this.newSearch)
            })
        }

    },
    methods: {
        filtrated(canzone){
            this.filterGenre = canzone
            console.log(this.filterGenre)
        },
        caricamentoMusica(){
            axios
            .get(this.apiURL)
            .then((risposta) => {
                // handle success
                this.musicaArray = risposta.data.response;
            })
            .catch(function (error) {
                // handle error
                console.log(error);
            });
        },
    },
}
</script>

<style lang="scss">
.container{
   display: flex;
}
.canzone{
    margin-top: 100px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
}
</style>
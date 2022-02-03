<template>
  <div class="select">
      <select
      :v-model="genre"
      @change="$emit('filtrated',genre)">
          <option value="">All</option>
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
      </select>

  </div>
</template>

<script>
export default {
    name: "Search",
    data(){
        return {
            genre:""
        } 
    }


}
</script>

<style>
select{
    display: inline-block;
}
</style>
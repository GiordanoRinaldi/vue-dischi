<template>
    <div class="albums container my-4">
      <div class="row row-cols-xl-5 row-cols-lg-4 row-cols-md-3 row-cols-sm-2">
        <div class="col- my-4" v-for="(elm, index) in albumsFiltered" :key="index">
          <Album class="mx-auto" :info="elm"/>
        </div>
      </div>
    </div>
</template>

<script>
import axios from "axios";
import Album from './Album.vue'



export default {
  name: "Albums",
  components: {
    Album,
  },
  props:['selectedGenre'],
  data(){
    return{
      albums: [],
      genre: [],
    }
  },
  created(){
    axios.get("https://flynn.boolean.careers/exercises/api/array/music")
    .then( (res) => {
      this.albums= res.data.response;
      this.albums.forEach(
        (elm) => {
          if (!this.genre.includes(elm.genre)){
            this.genre.push(elm.genre);
          }
        }
      );
      
    } );
  },
  computed: {
    albumsFiltered() {
      const arrFiltered = this.albums.filter(
        (elm) => {
          if(elm.genre == this.selectedGenre || this.selectedGenre == "" ) {
            return true
          }
          return false 
        }
      )

      return arrFiltered;
    }

    
  }

}
</script>

<style>

</style>
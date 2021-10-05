<template>
  <div id="app">
    <Header @filter="filterGenre" :genreLists="genreLists"/>
    <main>
      <Albums :selectedGenre="genreSelected" @genreList="genreAppear" />
    </main>
  </div>
</template>

<script>
import Albums from './components/Albums.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header,
    Albums
  },
  data(){
    return {
      genreSelected: "",
      genreLists: [],

    }
  },
  methods: {
    filterGenre(selectedGenre){
      this.genreSelected = selectedGenre
    },
    genreAppear(list) {
      this.genreLists = list;
    }
  },
}
</script>
<style lang="scss">

@import "./assets/style/common.scss";

#app{
  min-height: 100vh;
  background-color: $colorBody;
}


</style>

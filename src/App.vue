<template>
  <div id="app">
    <Header @filter="filterGenre" />
    <main>
      <Albums :selectedGenre="genreSelected" />
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
    }
  },
  methods: {
    filterGenre(selectedGenre){
      this.genreSelected = selectedGenre
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

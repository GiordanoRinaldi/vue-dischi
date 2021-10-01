<template>
  <div id="app">
    <Header/>
    <main>
      <Albums/>
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
  }
}
</script>
<style lang="scss">

@import "./assets/style/common.scss";

#app{
  height: 100vh;
  background-color: $colorBody;
}


</style>

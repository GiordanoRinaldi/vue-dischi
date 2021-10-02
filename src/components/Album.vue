<template>
  <div class="album text-center">
    <img :src="info.poster" :alt="info.title">
    <h4 style="text-transform:uppercase">{{info.title}}</h4>
    <div class="subtitle">
      <div>{{info.author}}</div>   
      <div>{{info.year}}</div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: "Album",
  props: ["info"]
}
</script>

<style lang="scss" scoped>
@import "../assets/style/common.scss";

  .album {
    width: 200px;
    height: 360px;
    background-color: $colorMainAlbum;
    padding: 20px;
  }

  h4{
    color: white;
  }
  .subtitle {
    color: #808080;
  }
  img{
    max-width: 100%;
    margin-bottom: 20px;
  }
</style>
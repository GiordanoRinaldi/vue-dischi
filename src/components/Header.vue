<template>
    <header>
        <div class="container-fluid d-flex justify-content-between">
            <img  src="../assets/image/spotify-logo.png" alt="logo spotify">

            <select class="form-select" aria-label="Default select example" v-model="genre" @change="$emit('filter', genre)" >
                <option value="">Filtra per genere </option>
                <option  value="Rock">Rock </option>
                <option  value="Jazz">Jazz </option>
                <option  value="Metal">Metal </option>
                <option  value="Pop">Pop </option>
            </select>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            genre: ""
        }
    }
}
</script>

<style lang="scss" scoped>

@import "../assets/style/common";

    header{
        height: 70px;
        background-color: $colorMainAlbum;

        .container-fluid{
            padding-top: 12.5px;

            img {
                height: 45px;
            }

        }

        
    }

    .form-select {
        width: 300px;
    }
</style>
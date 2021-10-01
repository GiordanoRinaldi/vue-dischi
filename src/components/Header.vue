<template>
    <header>
        <div class="container-fluid ms-2 ">
            <img  src="../assets/image/spotify-logo.png" alt="logo spotify">
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
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
</style>
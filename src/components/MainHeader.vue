<template>

    <header>

        <figure>
            <img class="logo" src="../assets/img/Spotify.png" alt="">
        </figure>

    </header>
  
</template>

<script>
export default {
    name: 'MainHeader'
}
</script>

<style lang="scss" scoped>

    header {
        padding: 15px;
        background-color: rgba($color: #ffffff, $alpha: 0.1);
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
    }

    .logo {
        width: 50px;
        }


</style>
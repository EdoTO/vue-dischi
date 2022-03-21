<template>
  <div class="card">
      <figure class="card-thumb">
          <img :src="album.poster" alt="">
      </figure>

      <div class="card-info">
          <h3>{{album.title}}</h3>
          <p>{{album.author}}</p>
          <p>{{album.year}}</p>
      </div>
  </div>
</template>

<script>
export default {
    name: 'AlbumCard',
    props: {
        album: {
            type: Object,
            required: true,
        }
    }
}
</script>

<style lang="scss" scoped>

.album {
    text-align: center;
    background-color: rgba($color: white, $alpha: 0.1);
    margin: 10px;
}

.card-thumb {


    img {
        width: 100%;
    }
}

</style>
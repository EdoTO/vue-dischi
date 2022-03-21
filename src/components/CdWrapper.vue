<template>
  <div class="cd-wrapper">
      <AlbumCard class="" v-for="(album, i) in cards" :key="i"  :album="album">
      </AlbumCard>
  </div>
</template>

<script>
import axios from 'axios'
import AlbumCard from './AlbumCard.vue'

export default {
    name: 'CdWrapper',
    components: {
        AlbumCard
    },
    data() {
        return{
            cards: []
        }
    },
    methods: {
        fetchAlbums: function () {

            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then(res => {
                this.cards = res.data.response
            })
            .catch(err => {
                console.log(err.response)
                this.cards = []
            })

        } 
    },
    created() {
        this.fetchAlbums()
    }
}
</script>

<style lang="scss" scoped>

    .cd-wrapper {
        display: flex;
        flex-wrap: wrap;
        gap: calc(5%/4);

        & > * {
            width: 19%;
        }
    }

</style>
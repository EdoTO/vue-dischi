<template>
  <main>
      <section>
          <div class="container">

              <CdWrapper />

          </div>
      </section>
  </main>
</template>

<script>
import CdWrapper from './CdWrapper.vue'

export default {
    name: 'MainContent',
    components: {
        CdWrapper,
    }
}
</script>

<style lang="scss" scoped>

    main {
        background-color: #1e2d38;
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .container {
        max-width: 1024px;
        margin: 150px auto;
    }


</style>
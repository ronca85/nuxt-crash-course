<template>
  <div class="container">
    <h1 class="c-title">
      Homepage title
    </h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus voluptatum expedita doloremque sed facere veritatis perspiciatis minus suscipit ab, aut, assumenda harum ea.</p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Homepage',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for corny dad jokes',
        }
      ]
    }
  },
  components: {
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 40px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>

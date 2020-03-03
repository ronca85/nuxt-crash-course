<template>
  <div class="container">
    <h1 class="c-title">
      About title
    </h1>
	<p class="c-text">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Assumenda, ipsam voluptatibus adipisci vitae nesciunt repudiandae quos corrupti hic voluptate facere, numquam eum. Magni sint necessitatibus, voluptates facilis repellat optio provident nisi omnis nostrum consectetur molestiae error aut ipsa veniam, dolorem ullam soluta explicabo fuga.</p>
  </div>
</template>

<script>
export default {
	head() {
		return {
			title: 'About the app',
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

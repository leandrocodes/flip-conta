<template>
  <div>
    <nuxt />
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Cairo:200,300,400,600,700,900&display=swap');
html,
body {
  font-family: 'Cairo', sans-serif;
}
</style>

<script>
export default {
  head() {
    return {
      title: this.title,
      link: [
        {rel: 'stylesheet', href:'https://fonts.googleapis.com/css?family=Cairo:200,300,400,600,700,900&display=swap'}
      ]
    }
  }
}
</script>

<template>
  <div class="container" v-cloak>
    <!-- v-cloak does not work for some reason link to notice [object Object] before the joke is loaded:
    http://localhost:3000/jokes/0189hNRf2g -->
    <AppHeader />
    <br />
    <nuxt />
  </div>
</template>
<script>
import AppHeader from '../components/AppHeader'

export default {
  components: {
    AppHeader,
  },
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  background: #f4f4f4;
}
a {
  color: #666;
  text-decoration: none;
}
ul {
  list-style: none;
}
.container {
  max-width: 800px;
  margin: 2rem auto;
  overflow: hidden;
  padding: 1rem 2rem;
  background: #fff;
}

[v-cloak] > * {
  display: none;
}
[v-cloak]::before {
  content: 'loading...';
}
</style>

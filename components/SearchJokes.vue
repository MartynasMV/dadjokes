<template>
  <form @submit.prevent="OnSubmit">
    <input type="text" v-model="text" placeholder="Search" />
    <input type="submit" value="Search jokes" />
  </form>
</template>

<script>
export default {
  name: 'SearchJokes',
  data() {
    return {
      text: '',
    }
  },
  methods: {
    OnSubmit() {
      this.$emit('search-text', this.text)
      this.text = ''
    },
  },
}
</script>

<style></style>

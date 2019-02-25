<template>
  <div>
    <h1>Create a Event, {{user.name}}</h1>
    <p>I am {{user.id}}</p>
    <p>There are {{catLength}} categores</p>
    <ul>
      <li v-for="(cat, index) in categories" :key="cat"> {{cat}} </li>
    </ul>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  computed: {
    catLength() {
      return this.$store.getters.catLength
    },
    ...mapState(['user', 'categories'])
  }
}
</script>

<style scoped>
</style>

<template>
  <button @click="addLike">Like</button>
  <button @click="addDislike">Dislike</button>
  <div>Количество like: {{like}}</div>
  <div>Количество dislike: {{dislike}}</div>
</template>

<script>
export default {
  data() {
    return {
      like: 0,
      dislike: 0
    }
  },
  methods: {
    addLike() {
      this.like++;
    },
    addDislike() {
      this.dislike++;
    }
  }
}
</script>

<style>

</style>
<template>
    <div class="post" v-bind:key="post.id" v-for="post in posts">
    <div>Название: <strong>{{post.title}}</strong></div>
    <div>Описание: <strong>{{post.text}}</strong></div>
  </div>
</template>

<script>
export default {
    props: {
        posts: {
            type: Array, 
            required: true,
        }
    }
}
</script>

<style>

</style>
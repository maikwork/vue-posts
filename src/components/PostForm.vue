<template>
    <form @submit.prevent>
    <input 
    v-bind:value="title"
    @input="title = $event.target.value"
    type="text" 
    class="input" 
    placeholder="Название">
    <input 
    v-bind:value="text"
    @input="text = $event.target.value"
    type="text" 
    class="input" 
    placeholder="Описание">
    <button @click="createPost" class="btn">Добавить</button>
  </form>
</template>

<script>
export default {

}
</script>

<style>

</style>
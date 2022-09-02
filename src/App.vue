<template>
  <post-form/>
  <post-list :posts="posts"/>
</template>

<script>
import PostForm from './components/PostForm.vue'
import PostList from './components/PostList.vue'
export default {
  components: { 
    PostForm, 
    PostList 
  },
  data() {
    return {
      posts: [
        {
          id: 0,
          title: "Название поста JS 1",
          text: "Описание поста 1",
        },
        {
          id: 1,
          title: "Название поста JS 2",
          text: "Описание поста 2",
        },
        {
          id: 2,
          title: "Название поста JS 3",
          text: "Описание поста 3",
        }
      ],
      title: '',
      text: '',
    }
  },
  methods: {
    createPost() {
      const new_post = {
        id: Date.now(), 
        title: this.title, 
        text: this.text
      }
      this.posts.push(new_post)
      this.title = this.text = ''
    }
  }
}
</script>

<style>
  * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  padding: 1vh 2vw;
}
form {
  display: flex;
  flex-direction: column;
}
.post {
  margin: 15px 0;
  padding: 15px 0px 15px 5px;
  border: 2px solid teal;
}
.input {
  width: 100%;
  padding: 10px;
  margin-bottom: 5px;
  border: 1.5px solid teal;
  color: black;
}
.btn {
  align-self: flex-end;
  background: none;
  border: 1.5px solid teal;
  margin-top: 5px;
  padding: 10px 5px;
  color: teal;
}
</style>
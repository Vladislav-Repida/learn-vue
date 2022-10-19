<template>
  <div class="container">
    <post-form @createPost="createPost" />
    <hr />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";
export default {
  components: {
    PostList,
    PostForm,
  },
  data() {
    return {
      posts: [{ title: "test", body: "test1", id: 1666194687371 }],
    };
  },
  methods: {
    createPost(post) {
      console.log(post);
      this.posts.push(post);
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;

  box-sizing: border-box;
}
.container {
  margin: 0 auto;
  width: 50%;
}
hr {
  margin: 40px 0;
}
</style>

<template lang="">
  <div class="wraper-form">
    <form @submit.prevent>
      <input
        v-model="post.title"
        class="input"
        type="text"
        placeholder="Название"
      />
      <input
        v-model="post.body"
        class="input"
        type="text"
        placeholder="Описание"
      />
      <my-button @click="createPost">Создать</my-button>
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("createPost", this.post);
      this.resetForm();
    },
    resetForm() {
      this.post = {
        title: "",
        body: "",
      };
    },
  },
};
</script>
<style scoped>
.input {
  display: block;
  padding: 10px 15px;
  border: 1px solid teal;
  margin-top: 16px;

  font-size: 16px;
  width: 100%;

  outline: none;
}
</style>

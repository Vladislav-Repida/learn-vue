<template>
  <div class="post">
    <div><strong>Название</strong> {{ post.title }}</div>
    <div><strong>Описание</strong> {{ post.body }}</div>
    <my-button @click="removePost" class="btn-remove-post">Удалить</my-button>
  </div>
</template>
<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
  methods: {
    removePost() {
      this.$emit("removePost", this.post.id);
    },
  },
};
</script>
<style scoped>
.post {
  padding: 15px;
  border: 2px solid red;
  margin-top: 15px;
  width: 100%;
}
.btn-remove-post {
  margin-top: 14px;
  font-size: 14px;
  padding: 5px 10px;
}
</style>

<template lang="">
  <div class="wraper-posts">
    <post-item v-for="post in posts" v-bind:key="post.id" :post="post" />
  </div>
</template>
<script>
import PostItem from "@/components/PostItem.vue";
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
  components: {
    PostItem,
  },
};
</script>
<style scoped></style>

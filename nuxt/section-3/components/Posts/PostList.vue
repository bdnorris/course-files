<template>
  <section class="featured-posts">
    <PostPreview 
      v-for="post in posts"
      :key="post.id"
      :id="post.id" 
      :is-admin="isAdmin"
      :title="post.title"
      :preview-text="post.previewText" 
      :thumbnail="post.thumbnail" />
  </section>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview'

export default {
  name: 'PostList',
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    },
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>

<style>
.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>

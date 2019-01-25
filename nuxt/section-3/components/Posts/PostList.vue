<template>
  <section class="featured-posts">
    <PostPreview 
      id="1" 
      :is-admin="isAdmin"
      title="Hello"
      preview-text="My post!" 
      thumbnail="https://source.unsplash.com/random/400x200" />
    <PostPreview 
      id="2" 
      :is-admin="isAdmin"
      title="Goodbye"
      preview-text="My post blah!" 
      thumbnail="https://source.unsplash.com/random/400x200" />
    <PostPreview 
      id="3" 
      :is-admin="isAdmin"
      title="Third thing"
      preview-text="My piss!" 
      thumbnail="https://source.unsplash.com/random/400x200" />
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

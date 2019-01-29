<template>
  <div class="posts-page">
    <PostList :posts="newPosts" />
  </div>
</template>

<script>
import PostList from '@/components/Posts/PostList'

export default {
  components: {
    PostList
  },
  asyncData(context, callback) {
    setTimeout(() => {
      return callback(null, {
        newPosts: [
          {
            id: '1',
            title: 'First Post',
            previewText: 'this is our first post',
            thumbnail: 'https://source.unsplash.com/random/400x200'
          },
          {
            id: '2',
            title: 'Second Post',
            previewText: 'this is our second post',
            thumbnail: 'https://source.unsplash.com/random/400x200'
          }
        ]
      })
    }, 2000)



    // asyncData ({ params }) {
    //   return axios.get(`https://my-api/posts/${params.id}`)
    //   .then((res) => {
    //     return { title: res.data.title }
    //   })
    // }
  }
}
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}


</style>


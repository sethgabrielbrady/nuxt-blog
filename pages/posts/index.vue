<template>
  <div class="posts-page">
    <PostList :posts="loadedPosts"/>
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
        callback(null, {
          loadedPosts: [
            {
              id: '1',
              title: 'First Post',
              previewText:'This is a first post',
              thumbnail:'https://www.brookings.edu/wp-content/uploads/2017/11/metro_20171121_tech-empowers-tech-polarizes-mark-muro.jpg'
            },
            {
              id: '2',
              title: 'Second Post',
              previewText:'This is a second post',
              thumbnail:'https://www.brookings.edu/wp-content/uploads/2017/11/metro_20171121_tech-empowers-tech-polarizes-mark-muro.jpg'
            },
            {
              id: '3',
              title: 'Third Post',
              previewText:'This is a third post',
              thumbnail:'https://www.brookings.edu/wp-content/uploads/2017/11/metro_20171121_tech-empowers-tech-polarizes-mark-muro.jpg'
            }
          ]
        })
      }, 1500)
    }
  }
</script>


<style scoped>
    .posts-page {
        display: flex;
        justify-content: center;
        align-content: center;
    }
</style>
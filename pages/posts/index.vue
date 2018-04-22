<template lang="html">
  <div class="posts-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
// import PostList from '@/components/Posts/PostList.vue'

export default {
    // components: {
    //   PostList
    // },
    // fetch(context) {
      // if (context.store.state.loadedPosts.length > 0) {
      //   return null;
      // }
    //   return new Promise((resolve, reject) => {
    //     setTimeout(() => {
    //       resolve({
    //         loadedPosts: [
    //           {
    //             id: "1",
    //             title: 'My Post',
    //             previewText: "This is our first Post!",
    //             thumbnail: 'http://nerdcrumble.com/wp-content/uploads/2017/04/best-tech-sites.jpg'
    //           },
    //           {
    //             id: "2",
    //             title: 'My Second Post',
    //             previewText: "This is our Second Post!",
    //             thumbnail: 'http://nerdcrumble.com/wp-content/uploads/2017/04/best-tech-sites.jpg'
    //           }
    //         ]
    //       })
    //     },1000)
    //     // reject(new Error())
    //   })
    //   .then(data => {
    //     context.store.commit('setPosts', data.loadedPosts)
    //   })
    //   // .then(data => {
    //   //   return data
    //   // })
    //   .catch(e => {
    //     context.error(e);
    //   });
    // },
    computed: {
      loadedPosts() {
        return this.$store.getters.loadedPosts
      }
    }
    // created() {
    //   this.$store.dispatch('setPosts', this.loadedPosts)
    // }
}
</script>

<style scoped lang="css">
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}


</style>

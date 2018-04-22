<template>
  <div class="home-page">
    <section class="intro">
      <h1>TAEWOO KIM BLOG</h1>
      <h3>Check my posts & projects ↓</h3>
      <div id="overlay"></div>
    </section>
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script type="text/javascript">
  // import PostList from '@/components/Posts/PostList'

  export default {
    // components: {
    //   PostList
    // },
    computed: {
      loadedPosts() {
        return this.$store.getters.loadedPosts
      }
    }
    // asyncData(context, callback) {
    //   setTimeout(() => {
    //     callback(null, {
    //       loadedPosts: [
    //         {
    //           id: "1",
    //           title: 'My Post',
    //           previewText: "This is our first Post!",
    //           thumbnail: 'http://nerdcrumble.com/wp-content/uploads/2017/04/best-tech-sites.jpg'
    //         },
    //         {
    //           id: "2",
    //           title: 'My Second Post',
    //           previewText: "This is our Second Post!",
    //           thumbnail: 'http://nerdcrumble.com/wp-content/uploads/2017/04/best-tech-sites.jpg'
    //         }
    //       ]
    //     })
    //   },1000)
    // }
    // data() {
    //   return{
    //     loadedPosts: []
    //   };
    // },
    // created() {
    //   setTimeout(()=> {
    //     this.loadedPosts = [
    //       {
    //         id: "1",
    //         title: 'My Post',
    //         previewText: "This is our first Post!",
    //         thumbnail: 'http://nerdcrumble.com/wp-content/uploads/2017/04/best-tech-sites.jpg'
    //       },
    //       {
    //         id: "2",
    //         title: 'My Second Post',
    //         previewText: "This is our Second Post!",
    //         thumbnail: 'http://nerdcrumble.com/wp-content/uploads/2017/04/best-tech-sites.jpg'
    //       }
    //     ]
    //   },1000)
    // }
  }
</script>


<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('~assets/images/main-page-background.jpg');
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  text-align: left;
  top: 20%;
  left: 5%;
  width: 90%;
  margin: 0 auto;
  font-size: 5em;
  font-weight: 800;
  letter-spacing: 0.05em;
  color: white;
  /* background-color: rgb(211, 211, 211); */
  padding: 10px;
  /* border-radius: 10px; */
  /* box-shadow: 3px 3px 3px black; */
  box-sizing: border-box;
  /* border: 1px solid black; */
  z-index: 10;
  line-height: 1em;
}

.intro h3 {
  position: absolute;
  width: 88%;
  text-align: right;
  top: 75%;
  color: white;
  z-index: 10;
}

#overlay {
  position:absolute;
  height:100%;
  width:100%;
  top:0;
  right:0;
  bottom:0;
  left:0;
  background:rgba(33,125,187,0.65);
  z-index:1
}

@media (min-width: 768px) {
  /* .intro h1 {
    font-size: 2rem;
  } */
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}


</style>

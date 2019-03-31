<template>
  <div id="home">
    <div class="banner">
      <img :src="require('@/assets/images/bg/background.webp')" alt="">
      <div class="title">
        <h1>Going Places</h1>
        <p>I haven’t been everywhere, but it’s on my list</p>
      </div>
    </div>
    <b-container>
      <div class="text-center" style="padding: 20px 0;">
        <p>Hey My name is Dzung<br/>I'm a web developer. Welcome to my house.</p>
      </div>
      <!-- categories -->
      <side-bar></side-bar>
      <!-- blog post -->
      <blog-post></blog-post>
    </b-container>
  </div>
</template>

<script>
// @ is an alias to /src
import SideBar from '../components/UI/SideBar.vue'
import BlogPost from '../components/UI/BlogPost.vue'
export default {
  name: 'home',
  components: {
    SideBar,
    BlogPost
  }
}
</script>

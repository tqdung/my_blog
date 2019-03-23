<template>
  <div id="home">
    <div class="title-blog">
      <h1>Going Places</h1>
      <p>I haven’t been everywhere, but it’s on my list</p>
    </div>
    <b-container>
      <div class="text-center" style="padding: 20px 0;">
        <p>I'm a web developer. Welcome to my house.</p>
      </div>
      <side-bar></side-bar>
    </b-container>
  </div>
</template>

<script>
// @ is an alias to /src
import SideBar from '../components/UI/SideBar.vue'
export default {
  name: 'home',
  components: {
    SideBar
  }
}
</script>
<style lang="scss" scoped>
#home {
  .title-blog {
    color: white;
    background-image: url('..//assets/images/bg/background.webp');
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 475px;
  }
}
</style>

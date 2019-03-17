<template>
  <div id="home">
    <!-- <img width="100%;" :src="require('@/assets/images/bg/background.webp')" alt=""> -->
    <!-- <div class="background-image"></div> -->
    <div class="banner">
      <h1>Going Places</h1>
      <p>I haven’t been everywhere, but it’s on my list</p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'home',
  components: {
  }
}
</script>
<style lang="scss" scoped>
#home {
  .banner {
    background-image: url('..//assets/images/bg/background.webp');
    background-size: cover;
    background-repeat: no-repeat;
    width: 100%;
    // height: 480px;
    padding-top: 50px;
    color: white;
  }
}
@media screen and (max-width: 480px) {
  #home {
    .banner {
      // height: 236px;
    }
    h1 {
      font-size: 70px;
    }
    p {
      font-size: 20px;
    }
  }
}
</style>

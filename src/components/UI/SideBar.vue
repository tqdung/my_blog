<template>
  <div id="main-sidbar">
      <b-container>
          <b-row>
            <b-col sm="4" md="4" cols="12" class="banner" v-for="cat in categories" :key="cat.name">
                <div class="banner-item">
                    <img :src="cat.image" alt="banner-item">
                    <div class="banner-item-name">
                      <router-link :to="cat.name">{{cat.name}}</router-link>
                    </div>
                </div>
            </b-col>
          </b-row>
      </b-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      categories: [
        {
          image: require('@/assets/images/category/travel.webp'),
          name: 'Travel'
        },
        {
          image: require('@/assets/images/category/eat.webp'),
          name: 'Eats'
        },
        {
          image: require('@/assets/images/category/relax.webp'),
          name: 'Relax'
        }
      ]
    }
  }
}
</script>
<style lang="scss">
@import '@/assets/scss/_variable.scss';
#main-sidbar {
  width: 100%;
  height: auto;
  margin-bottom: 20px;

  .banner {
    padding: 0;
  }

  .banner-item {
    padding: 8px;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;

    &-name {
        width: 150px;
        height: 50px;
        background: white;
        position: absolute;
        color: $blue-text;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    img {
        width: 100%;
    }
    a {
      text-decoration: none;
    }
}
}
</style>

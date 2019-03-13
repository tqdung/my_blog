<template>
    <header id="header_top">
        <b-container>
            <b-row>
                <b-col sm="6" cols="12">
                    <div class="header-left">
                        <ul>
                            <li><a href="#">Home</a></li>
                            <li><a href="#">About</a></li>
                            <li><a href="#">Travel</a></li>
                            <li><a href="#">Eat</a></li>
                            <li><a href="#">Relax</a></li>
                            <li><a href="#">Videos</a></li>
                        </ul>
                    </div>
                </b-col>
                <b-col sm="6" cols="12">
                    <div class="header-right">
                        <ul>
                            <li><a href="#"><img :src="require('@/assets/images/icons/facebook.webp')" alt="facebook"></a></li>
                            <li><a href="#"><img :src="require('@/assets/images/icons/instagram.webp')" alt="instagram"></a></li>
                            <li><a href="#"><img :src="require('@/assets/images/icons/pinterest.webp')" alt="pintrest"></a></li>
                            <li><a href="#"><img :src="require('@/assets/images/icons/twister.webp')" alt="twister"></a></li>
                        </ul>
                        <div class="toggle" @click="openMenu = !openMenu">
                            <i class="fa fa-bars"></i>
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-container>
        <div class="mobile-menu" :class="{show: openMenu}">
            <div  @click="openMenu =  false" class="placeholder"></div>
            <div class="menu">
            <ul>
                <li><a>HOme</a></li>
                <li><a>HOme</a></li>
                <li><a>HOme</a></li>
                <li><a>HOme</a></li>
                <li><a>HOme</a></li>
            </ul>
            </div>
        </div>
    </header>
</template>

<script>
export default {
  data () {
    return {
      openMenu: false
    }
  }
}
</script>

<style>

</style>

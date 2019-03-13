<template>
  <div class="home">
    <header-page></header-page>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderPage from '@/components/layouts/Header.vue'

export default {
  name: 'home',
  components: {
    HeaderPage
  }
}
</script>

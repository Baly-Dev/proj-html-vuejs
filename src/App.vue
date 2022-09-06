<template>
  <div id="app" class="main">
    <TheHeader />
    <TheMain />
  </div>
</template>

<script>
import TheHeader from './components/header/TheHeader.vue'
import TheMain from './components/TheMain.vue'
export default {
  name: 'App',
  components:{
    TheHeader,
    TheMain
  }
}
</script>

<style lang="scss">
@import '@/assets/scss/framework.scss';
@import '@/assets/scss/global.scss';

.main{
  width: 100%;
}

</style>

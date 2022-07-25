<template>
    <div id="root">
      <TheHeader />
      <TheJumbotron />
      <TheMain/> 
      <TheFooter/>
    </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue'
import TheMain from './components/TheMain.vue'
import TheFooter from './components/TheFooter.vue'
import TheJumbotron from './components/TheJumbotron.vue'

export default {
  name: 'App',
  components: {
    TheHeader,
    TheMain,
    TheFooter,
    TheJumbotron,
  }
}

</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>

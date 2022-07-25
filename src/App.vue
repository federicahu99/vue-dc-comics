<template>
    <div id="root">
      <TheHeader />
      <TheJumbotron />
      <TheMain>
        <ComicsSection />  
      </TheMain>
      <TheBanner />
      <TheFooter/>
    </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue'
import TheMain from './components/TheMain.vue'
import TheFooter from './components/TheFooter.vue'
import TheJumbotron from './components/TheJumbotron.vue'
import ComicsSection from './components/ComicsSection.vue'
import TheBanner from './components/TheBanner.vue'

export default {
  name: 'App',
  components: {
    TheHeader,
    TheMain,
    TheFooter,
    TheJumbotron,
    ComicsSection,
    TheBanner,

}
  }

</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>

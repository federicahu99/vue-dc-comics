<template>
  <div id="bg-dark">
    <div class="container">
      <ComicsSection />
    </div>
  </div>
</template>

<script>
import ComicsSection from './ComicsSection.vue'

export default {
    name: 'TheMain',
    components: {
    ComicsSection,
    }
}
</script>

<style lang="scss" scoped>
    #bg-dark {
        background-color: #1c1c1c;
        min-height: 150px;

        h1{
          color:white;
          padding: 35px 0;
        }
    }
</style>
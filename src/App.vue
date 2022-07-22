<template>
  <BaseHeader />
</template>

<script>
import BaseHeader from './components/BaseHeader.vue'

export default {
  name: 'App',
  components: {
    BaseHeader,
  },
  data(){ 
    return {
      links: [
  {
    text: 'Characters',
    url: '#',
    current: false,
  },
  {
    text: 'Comics',
    url: '#',
    current: true,
  },
  {
    text: 'Movies',
    url: '#',
    current: false,
  },
  {
    text: 'TV',
    url: '#',
    current: false,
  },
  {
    text: 'Games',
    url: '#',
    current: false,
  },
  {
    text: 'Collectibles',
    url: '#',
    current: false,
  },
  {
    text: 'Videos',
    url: '#',
    current: false,
  },
  {
    text: 'Fans',
    url: '#',
    current: false,
  },
  {
    text: 'News',
    url: '#',
    current: false,
  },
  {
    text: 'Shop',
    url: '#',
    current: false,
  }
  ]}
  }
}

</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>

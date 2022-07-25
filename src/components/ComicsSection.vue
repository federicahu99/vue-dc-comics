<template>
  <div class="container">
    <h2>CURRENT SERIES</h2>
    <div class="cards">
        <TheComic />
    </div>

  </div>
</template>

<script>

import TheComic from './TheComic.vue'
export default {
    name: 'ComicsSection',
    components:{
        TheComic,
    }
}

</script>

<style lang="scss" scoped>
    h2 {
        background-color: dodgerblue;
        display: inline-block;
        color:white;
        padding: 10px;
        margin-top: -20px;
    }

    .cards {
        margin-top: 30px;
        display: flex;
        justify-content: space-between;
       

        figure {
            flex-basis: 25%;

            img {
                object-fit: cover;
                object-position: top;
                height: 180px;
                width: 180px;
            }

            h4 {
                color: white;
                text-transform: uppercase;
            }
        }
    }
</style>
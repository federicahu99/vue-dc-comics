<template>
    <div>
        <h2>CURRENT SERIES</h2>
        <div class="cards">
            <TheComic class="comic-container"
            v-for="(comic, i) in comicsList" 
            :key="i" 
            :comic-src="comic.thumb" 
            :comic-alt="comic.series" 
            :comic-series="comic.series" />
        </div>
        <a href="#" id="more">Load for more</a>
    </div>
</template>

<script>

import TheComic from './TheComic.vue'
import axios from 'axios'

export default {
    name: 'ComicsSection',
    components:{
        TheComic,
    }, data() { //axios
        return {
            comicsList: [],
        }
    }, methods: {
        getJSON(){
            return axios.get('/dc-comics.json') //cartella pubblic
            .then(res => this.comicsList=(res.data))
            .catch(err => console.log(err))
        }
    }, mounted(){
        this.getJSON()
    }
}

</script>

<style lang="scss" scoped>
    h2 {
        background-color: dodgerblue;
        display: inline-block;
        color:white;
        padding: 10px;
        margin-top: -30px;
    }

    .cards {
        margin-top: 30px;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
       

        .comic-container {
            flex-basis: calc(100% / 6 - 20px);
            padding: 10px;
        }
    }

    #more {
        display: flex;
        justify-content: center;
        display: inline-block;
        margin: 30px 0;
        background-color: dodgerblue;
        color: white;
        text-transform: uppercase;
        padding: 5px 15px;
    }
</style>
<template>
    <div>
        <h2>CURRENT SERIES</h2>
        <div class="cards">
            <TheComic v-for="(comic, i) in comicsList" 
            :key="i" 
            :comic-src="comic.thumb" 
            :comic-alt="comic.series" 
            :comic-type="comic.type" />
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
            .then(res => this.comicsList(res.data))
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

    #more {
        display: inline-block;
        margin: 30px auto;
        background-color: dodgerblue;
        color: white;
        text-transform: uppercase;
        padding: 5px 15px;
    }
</style>
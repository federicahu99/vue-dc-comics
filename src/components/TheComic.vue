<template>
   <figure>
        <a href="#">
            <img 
                :src="comicSrc" 
                :alt="comicAlt">
            <figcaption>
                {{ comicSeries }}
            </figcaption>
        </a>
   </figure>
</template>

<script>
export default {
    name: 'TheComic',
    props: {
        comicSrc: String,
        comicAlt: String,
        comicSeries: String,
    }
}
</script>

<style lang="scss" scoped>
    figure{
        width: 140px;

        img {
            object-position: top;
            object-fit:cover;
            height: 130px;
            width: 130px;

        }
        figcaption {
            color: white;
            text-transform: uppercase;
            font-size: 12px;
            margin-top: 10px;
        }
    }
</style>
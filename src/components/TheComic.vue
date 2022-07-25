<template>
   <figure>
        <img :src="require(comicSrc)" :alt="comicAlt">
        <figcaption>{{comicType}}</figcaption>
   </figure>
</template>

<script>
export default {
    name: 'TheComic',
    props: {
        comicSrc: String,
        comicAlt: String,
        comicType: String,
    }
}
</script>

<style lang="scss" scoped>
    figure{
        flex-basis : calc(100% /6);

        img {
            object-position: top;
            object-fit: cover;
            height: 180px;
            width: 180px;

        }
        figcaption {
            color: white;
            text-transform: uppercase;
        }
    }
</style>
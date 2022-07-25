<template>
   <figure>
    <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX" alt="">
    <figcaption>action comics</figcaption>
   </figure>
</template>

<script>
export default {
    name: 'TheComic'
}
</script>

<style lang="scss" scoped>
    figure{
        flex-basis : 25%;

        img {
            object-position: top;
            object-fit: cover;
            width: 180px;
            height: 180px;

        }
        figcaption {
            color: white;
            text-transform: uppercase;
        }
    }
</style>
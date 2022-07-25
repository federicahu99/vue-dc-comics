<template>
  <div>
    <figure v-for="shop in bannerShop" :key="shop.src">
        <a href="#" class="banner-flex">
            <img :src="require(shop.src)" :alt="shop.text">
            <h3> {{shop.text}}</h3>
        </a>
    </figure>
  </div>
</template>

<script>
export default {
    name: 'TheBanner',
    data() {
        return {
            bannerShop: [
                {
                    src: '../assets/img/buy-comics-digital-comics.png',
                    text: 'digital comics',
                },
                {
                    src: '../assets/img/buy-comics-merchandise.png',
                    text: 'digital merchandise',
                },
                {
                    src: '../assets/img/buy-comics-dc-power-visa.png',
                    text: 'dc power visa',
                },
                {
                    src: '../assets/img/buy-comics-subscritions.png',
                    text: 'subscritions',
                },
                {
                    src: '../assets/img/buy-comics-shop-locator.png',
                    text: 'comic shop locator',
                }
            ]

        }
    }
}
</script>

<style lang="scss" scoped>
    figure {
        margin: 20px;
        color: white;
        height: 100px;

        .banner-flex{
            display: flex;
            justify-content: space-between;
        }
    }
</style>
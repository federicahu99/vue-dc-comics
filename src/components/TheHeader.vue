<template>
  <header class="container">
    <div id="header-flex">
        <figure>
            <img src="../assets/img/dc-logo.png" alt="logo DC">
        </figure>
        <nav>
            <ul>
                <li v-for="link in links" :key="link.text">
                <a 
                    :href="link.url"
                    :class="{active: link.current}"> 
                    {{ link.text }} 
                </a>
                </li>
            </ul>
        </nav>
    </div>
  </header>
</template>

<script>
export default {
    name: 'BaseHeader',
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

<style lang="scss" scoped>
header {
    height: 80px;
    
    #header-flex{
        height: 80%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    figure {
        height: 90%;

        img{
            height: 90%;
            margin-top: 7px;
        }
    }

    ul {
        display: flex;
        
        li{
            padding: 10px;
            margin-right: 10px;
            text-transform: uppercase;
            font-size: 10px;
            font-weight: bolder;
        }
    }
}
</style>
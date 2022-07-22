<template>
  <header class="container">
    <div>
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
    name: 'BaseHeader'
}
</script>

<style lang="scss" scoped>
header {
    height: 150px;
    display: flex;
    justify-content: space-between;

    figure {
        height: 50pxs;
    }
}
</style>
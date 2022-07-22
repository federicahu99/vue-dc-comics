<template>
  <header>
    <figure>
        <img src="../assets/img/dc-logo.png" alt="">
    </figure>
    <nav>
        <ul>
            <li v-for="link in links" :key="link.text">
            <a 
                :href="link.url"> 
                {{ link.text }} 
            </a>
            </li>
        </ul>
    </nav>
  </header>
</template>

<script>
export default {
    name: BaseHeader
}
</script>

<style>

</style>
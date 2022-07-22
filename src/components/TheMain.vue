<template>
  <div id="bg-dark">
    <div class="container">
      <h1>Content goes here</h1>
    </div>
  </div>
</template>

<script>
export default {
    name: 'TheMain'
}
</script>

<style lang="scss" scoped>
    #bg-dark {
        background-color: black;
        min-height: 150px;

        h1{
          color:white;
          padding: 35px 0;
        }
    }
</style>
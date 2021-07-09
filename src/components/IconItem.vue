<template>
  <div class="IconItem text-center p-4">
    <img :src="iconInfo.poster" alt="">
    <h5 class="text-uppercase fs-5 fw-bolder pt-2"> {{iconInfo.title}} </h5>
    <p class="text-secondary mt-3"> {{iconInfo.author}} </p>    
    <p class="text-secondary"> {{iconInfo.year}} </p>
  </div>
</template>

<script>
export default {
  name : 'IconItem',
  props : ["iconInfo"]
}
</script>

<style lang="scss">
  .IconItem{
    background-color: #2e3a46;
    height: 100%;

    img{
      width: 100%;
    }

  }
</style>


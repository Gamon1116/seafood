<template>
  <div>
    <button @click="productPage"> 소개페이지</button>
    <br>
    <span class="product">{{ title }}</span>
  </div>
</template>

<script>
export default {
  name: 'ProductPage',
  data() {
    return {
      title: ''
    }
  },
  methods: {
    productPage (){
      this.title = '여기에 넣을껀데'

    }
  }
}
</script>

<style>

</style>
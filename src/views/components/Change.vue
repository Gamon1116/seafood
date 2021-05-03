<template>
    <div>
        <div>
            <button @click="ChangePage"> 다른 div 로 넣는방법은?</button>
            <br>
        </div>
        <div class="product">
            {{ title }}
        </div>
    </div>
</template>

<script>
export default {
  name: 'change',
  data() {
    return {
      title: ''
    }
  },
  methods: {
    ChangePage (){
      this.title = '이런식으로 감싸서 넣는다면?'

    }
  }
}
</script>

<style>

</style>
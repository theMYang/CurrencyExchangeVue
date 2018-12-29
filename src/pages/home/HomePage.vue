<template>
  <currency-show-block></currency-show-block>
</template>

<script>
import CurrencyShowBlock from './components/CurrencyShowBlock'
import axios from 'axios'

export default {
  name: 'HomePage',
  components: {
    CurrencyShowBlock
  },
  methods:{
    getCurrencyShow(){
      axios.get('/home/testMock.js')
      .then(this.getCurrencyShowInfo)
    },
    getCurrencyShowInfo(res){
      console.log(res)
    }
  },
  mounted(){
    this.getCurrencyShow()
  }
}
</script>

<style>
   
</style>

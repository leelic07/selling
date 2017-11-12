<template>
  <div>
    I am seller
  </div>
</template>

<script type="text/ecmascript-6">
  import axios from 'axios'
  export default {
    data() {
      return {
        seller: {}
      }
    },
    methods: {
      getSeller(){
        axios.get('/seller').then(res => {
          if (res.data.errno == 0) {
            console.log(res.data.data);
          }
        })
      }
    },
    mounted(){
      this.getSeller();
    }
  }
</script>

<style type="text/stylus" lang="stylus">

</style>

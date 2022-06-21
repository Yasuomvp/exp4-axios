<script>



export default {
  data(){
    return {
      boboData:null
    }
  },
  methods:{
    getData(){
      this.$axios.get('https://api.github.com/users/bwhyman').then(res=>{

            this.boboData = res.data

            console.log(this.boboData)
      })
    }
  }
}


</script>
<template>
  <button type="button" @click="getData">tap me</button>
  <br>
  {{boboData}}
</template>

<template>
  <h1>Hi {{name}}</h1>
  <MultiModal :head="head" :content="content" :theme="theme" />
</template>

<script>
import MultiModal from "./components/MultiModel.vue"
export default {
  data(){
    return{
      name : "Kevin",
      head : "Login Success",
      content : "Welcome,Traveller",
      theme : "success"
    }
  },
  components:{
    MultiModal
  }
}
</script>

<style scoped>
  h1{
    color: aqua;
  }
</style>
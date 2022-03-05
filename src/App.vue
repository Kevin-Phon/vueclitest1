<template>
  <h1>Hi {{name}}</h1>
  <div v-if="showModal">
    <MultiModal :head="head" :content="content" :theme="theme" @close="showModal=false" />
  </div>
  <button @click="showModal=true">open modal</button>
</template>

<script>
import MultiModal from "./components/MultiModel.vue"
export default {
  data(){
    return{
      name : "Kevin",
      head : "Login Success",
      content : "Welcome,Traveller",
      theme : "success",
      showModal : false
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
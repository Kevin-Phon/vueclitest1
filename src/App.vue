<template>
  <h1>Hi {{name}}</h1>
  <div v-if="showModal">
    <MultiModal :theme="theme" @close="showModal=false" >
      <h1>Login Success</h1>
      <p>Welcomr,Traveller</p>

      <!-- slot with conditions -->
      <template v-slot:links>
        <a href="">Sign Up</a>
        <a href="">Register</a>
      </template>

    </MultiModal>
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
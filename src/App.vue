<template>
  <h1>Hi {{name}}</h1>

  <!-- one Modal -->
  <div v-if="showModal">
    <MultiModal :head="head" :content="content" :theme="theme" @close="showModal=false"/>
  </div>



  <!-- another Modal -->
  <div v-if="showanotherModal">
    <MultiModal :firstname="firstname" :lastname="lastname" :age="age" :color="color" @closeanother="showanotherModal=false"/>
  </div>

  <button @click="showModal=true">open modal</button> <br><br>
  <button @click="showanotherModal=true">open another modal</button>

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
      firstname : "Kevin",
      lastname : "Phon",
      age : "23",
      color : "delete",
      showModal : false,
      showanotherModal : false,
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
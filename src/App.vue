<template>
  <h1>Hi {{name}}</h1>

  <!-- one Modal -->
  <div v-if="showModal">
    <MultiModal :head="head" :content="content" :theme="theme" @close="showModal=false"/>
  </div>

  <!-- another Modal -->
  <div v-if="showanotherModal">
    <MyModal :title="title" :text="text"  :color="color" @closeanother="showanotherModal=false"/>
  </div>

  <button @click="showModal=true">open modal</button> <br><br>
  <button @click="showanotherModal=true">open another modal</button>

</template>

<script>
import MultiModal from "./components/MultiModel.vue"
import MyModal from "./components/MyModal.vue"
export default {
  data(){
    return{
      name : "Kevin",
      head : "Login Success",
      content : "Welcome,Traveller",
      theme : "success",
      title : "Are you sure you wnat to delete",
      text : "Delete done",
      color : "delete",
      showModal : false,
      showanotherModal : false,
    }
  },
  components:{
    MultiModal,
    MyModal
  }
}
</script>

<style scoped>
  h1{
    color: aqua;
  }
</style>
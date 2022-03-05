<template>
  <h1>Hi {{name}}</h1>
  <MultiModal head="Login Success" content="Welcome,Traveller" theme="success" />
</template>

<script>
import MultiModal from "./components/MultiModel.vue"
export default {
  data(){
    return{
      name : "Kevin"
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
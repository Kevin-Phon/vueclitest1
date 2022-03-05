<template>

    <!-- one Modal -->
  <div class="backdrop" @click.self="closeModal" @click="closeanotherModal">

      <div class="modal" :class="{success:theme==='success',danger:theme==='danger'}">
          <h1>{{head}}</h1>
          <p>{{content}}</p>
      </div>

      <div class="anothermodal" :class="{delete:color==='delete'}">
            <h3>{{firstname}}</h3>
            <h3>{{lastname}}</h3>
            <h3>{{age}}</h3>
        </div>

  </div>

    <!-- another modal -->
  <!-- <div class="backdrop2" @click.self="closeanotherModal">
      
        <div class="anothermodal" :class="{delete:color==='delete'}">
            <h3>{{firstname}}</h3>
            <h3>{{lastname}}</h3>
            <h3>{{age}}</h3>
        </div>

  </div> -->

</template>

<script>
export default {
    props:['head','content','theme','firstname','lastname','age','color'],
    methods:{
        closeModal(){
            this.$emit('close')
        },
        closeanotherModal(){
            this.$emit('closeanother')
        }
    },
    
}
</script>

<style scoped>
    .backdrop{
        position : fixed;
        top : 0;
        background: rgba(0, 0, 0, 0.5);
        width : 100%;
        height: 100%;
    }
    .backdrop2{
        position : fixed;
        top : 0;
        background: rgba(0, 0, 0, 0.5);
        width : 100%;
        height: 100%;
    }
    .modal{
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background-color: white;
        border-radius: 10px;
    }
    .anothermodal{
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background-color: white;
        border-radius: 10px;
    }
    .success{
        background-color: green;
        color: white;
    }
    .danger{
        background-color: crimson;
        color : white;
    }
    .delete{
        background-color: aqua;
        color : white;
    }
</style>
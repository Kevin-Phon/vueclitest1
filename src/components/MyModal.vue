<template>
  
    <!-- another modal -->
  <div class="backdrop2" @click.self="closeanotherModal">
      
        <div class="anothermodal" :class="{delete:color==='delete'}">
            <h1>{{title}}</h1>
            <p>{{text}}</p>
        </div>

  </div>
</template>

<script>
export default {
    props:['title','text','color'],
    methods:{
        closeanotherModal(){
            this.$emit('closeanother')
        }
    }
}
</script>

<style>
    .backdrop2{
        position : fixed;
        top : 0;
        background: rgba(0, 0, 0, 0.5);
        width : 100%;
        height: 100%;
    }
    .anothermodal{
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background-color: white;
        border-radius: 10px;
    }
    .delete{
        background-color: crimson;
        color : white;
    }
</style>
<template>
  <div class="backdrop" @click.self="closeModal">
      <div class="modal" :class="{success:theme==='success',danger:theme==='danger'}" >
          <!-- <slot/> -->
          <slot>
              <!-- default (if there is no data,the data here will show as default. so use <slot></slot>) -->
          </slot>

        <!-- slot with conditions -->
          <slot name="links"/>
      </div>
  </div>
</template>

<script>
export default {
    props:['head','content','theme'],
    methods:{
        closeModal(){
            this.$emit('close')
        }
    }
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
    .modal{
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
</style>
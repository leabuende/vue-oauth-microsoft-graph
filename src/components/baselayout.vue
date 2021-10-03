<template>
  <div class="layout">
    <baseheader/>
    <slot></slot>
      <basefooter/>
  </div>
</template>


<script>
import basefooter from './basefooter.vue'
import baseheader from './baseheader.vue'

export default {
  name: 'baselayout',
  components:{
      basefooter,
      baseheader
  }
 
}
</script>

<style scoped>
.footer{
   background-color: #fafafa;
   padding:30px;
}
</style>

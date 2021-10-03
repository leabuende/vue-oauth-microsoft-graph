<template>
  <div class="button">
      <button :class="color" :disabled="disabled">
      {{text}}
      </button>
    
  </div>
</template>

<script>
export default {
  name: 'basebutton',
  props:{
      'text': String,
      'disabled': Boolean,
      'color':{
          type: String,
          default:'primary'
      }
  }
 
}
</script>

<style scoped>
.home{
  min-height: 100vh;
}
.danger{
    background-color: red;
    border: 1px solid red;
}
.warn{
    background-color: orange;
}
.primary{
    background-color: green;
}
button{
    padding:10px;
    color:white;
    border:none;
    transition: 0.5s;
}
button:hover{
    border-radius: 25px;
}
button:focus{
    border-radius: 25px;
     background-color:white;
    color:salmon;
    border: 1px solid salmon;
}
</style>

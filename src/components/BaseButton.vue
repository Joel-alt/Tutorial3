<template>
  <button type="button"  class="button1" :class="color">
    Hello
    <slot/>
  </button>
</template>

<script>

export default {
  name: 'BaseButton',
  props: ['color']
}
</script>

<style>
.button1{
  border-bottom-color: forestgreen;
  height: 80px;
  width: 80px;
  border-radius: 5%;
  color: white;
  border:none;
  margin: 3px;
}

.button1:hover{
  background-color: darkgreen;
}

.button1:focus{
  background-color: black;
}

.button1:disabled{
  background-color: grey;
}

.primary{
  background-color: forestgreen;
}

.warn{
  background-color: orange;
}

.danger{
  background-color: red;
}
</style>
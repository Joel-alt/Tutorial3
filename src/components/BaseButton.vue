<template>
  <button type="button" disabled class="button1">
    Base Button with custom margin
  </button>
</template>

<script>

export default {
  name: 'BaseButton'
}
</script>

<style>
.button1{
  background-color: forestgreen;
  border-bottom-color: forestgreen;
  height: 40px;
  border-radius: 5%;
  color: white;
  border:none;
}

.button1:hover{
  background-color: darkgreen;
}

.button1:focus{
  background-color: red;
}

.button1:disabled{
  background-color: grey;
}
</style>
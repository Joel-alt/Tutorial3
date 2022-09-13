<template>
  <div class="header">
    <h1><a href="/">Mon compte</a></h1>
    <h1>Not yet logged in</h1>
  </div>
</template>

<script>
export default {
  name: 'BaseHeader',
}
</script>

<style>
.header{
  background-color: forestgreen;
  margin: 0;
  flex-basis: 10vh;
  display: flex;
  justify-content: space-between;
}

</style>
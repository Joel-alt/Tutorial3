<template>
  <div class="body">
    <h1>hello</h1>
    <BaseButton/>
  </div>
</template>

<script>
import BaseButton from "@/components/BaseButton";
export default {
  name: 'HomePage',
  components: {BaseButton}
}
</script>

<style>
.body{
  flex-basis: 80vh;
  margin: 0;
}
</style>
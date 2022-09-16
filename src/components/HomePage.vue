<template>
  <div class="body">
    <h1>hello</h1>
    <AsyncButton/>
    <BaseButton color="primary"/>
    <BaseButton color="warn"/>
    <BaseButton color="danger"/>
  </div>
</template>

<script>
import BaseButton from "@/components/BaseButton";
import AsyncButton from "@/components/AsyncButton";
export default {
  name: 'HomePage',
  components: {AsyncButton, BaseButton}
}
</script>

<style>
.body{
  flex-basis: 80vh;
  margin: 0;
}
</style>
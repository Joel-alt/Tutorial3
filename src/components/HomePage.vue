<template>
  <div class="body">
    <h1>hello</h1>
    <AsyncButton :onClick="createPromise"></AsyncButton>
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
  data() {
    return{
      count :2000
    }
  },
  components: {AsyncButton, BaseButton},
  methods:{
    createPromise () {
      const promise1 = new Promise((resolve) => {
        setTimeout(resolve, this.count);
      });
      this.count+=1000
      return promise1
    }
  }
}
</script>

<style>
.body{
  flex-basis: 80vh;
  margin: 0;
}
</style>
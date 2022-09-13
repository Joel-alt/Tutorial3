<!-- template of file src/App.vue -->
<template>
  <div class="page">
    <BaseHeader />
    <HomePage />
    <BaseFooter />
  </div>
</template>


<script>
import BaseHeader from "@/components/BaseHeader";
import HomePage from "@/components/HomePage.vue";
import BaseFooter from "@/components/BaseFooter";
export default {
  name: 'App',
  components: {
    BaseHeader,
    HomePage,
    BaseFooter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.page{
  display: flex;
  flex-direction: column;
  margin:0;
}
</style>

<!-- template of file src/App.vue -->
<template>
  <div class="page">
    <BasicLayout>
    <HomePage />
    </BasicLayout>
  </div>
</template>


<script>
import HomePage from "@/components/HomePage.vue";
import BasicLayout from "@/components/BasicLayout";
export default {
  name: 'App',
  components: {
    BasicLayout,
    HomePage
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

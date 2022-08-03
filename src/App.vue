<template>
<!--  <img alt="Vue logo" src="./assets/logo.png">-->
  <HomePage  msg="Welcome to Your Vue.js App"/>
  <FormWrapper group="update-form" v-cloak/>
</template>

<script>
import HomePage from "@/components/Home";
import FormWrapper from "@/components/Form/Wrapper";

export default {
  name: 'App',
  components: {
    FormWrapper,
    HomePage,
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
  margin-top: 60px;
}
</style>

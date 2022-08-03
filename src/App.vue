<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <FormWrapper group="update-form" v-slot="form_props">
    <div class="card">
      <div class="card-header">
        <HomePage  msg="View Form Components" class="mb-3"/>
      </div>
      <div class="card-body">
        <div class="mb-3 text-start">
          <label for="full_Name" class="form-label">Full Name : {{ form_props.fields.full_name }}</label>
          <input type="text" v-model="form_props.fields.full_name"
                 class="form-control" id="full_Name" placeholder="Full Name">
        </div>
      </div>
    </div>

  </FormWrapper>
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

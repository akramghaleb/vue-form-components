<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <FormWrapper group="update-form" v-slot="form_props">
    <div class="card">
      <div class="card-header">
        <HomePage  msg="View Form Components" class="mb-3"/>
      </div>

      <div class="card-body">
        <TextInput label="Full Name"
          :group="form_props.group"
          name="first_name"
          v-model:value="form_props.fields.first_name"
          current-value="Akram Ghaleb"
          :focus="true"
          placeholder="First Name"
          autocomplete="given-name"
          />
        <EmailInput label="Email"
                   :group="form_props.group"
                   name="email"
                   v-model:value="form_props.fields.email"
                   current-value=""
                   :focus="false"
                   placeholder="akramghammari@gmail.com"
                   autocomplete="given-name"
        />
        <PasswordInput label="Password"
                    :group="form_props.group"
                    name="password"
                    v-model:value="form_props.fields.password"
                    current-value=""
                    :focus="false"
                    placeholder=""
                    autocomplete="given-name"
        />
      </div>
    </div>

  </FormWrapper>
</template>

<script>
import HomePage from "@/components/Home";
import FormWrapper from "@/components/Form/Wrapper";
import TextInput from "@/components/Form/Input/Text";
import EmailInput from "@/components/Form/Input/Email";
import PasswordInput from "@/components/Form/Input/Password";

export default {
  name: 'App',
  components: {
    PasswordInput,
    TextInput,
    FormWrapper,
    HomePage,
    EmailInput
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

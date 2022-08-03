<template>
  <form novalidate>
    <slot
        :group="group"
        :fields="fields"
        :validation="validationBag"
    >
    </slot>
  </form>
</template>

<script>
export default {
  name: "FormWrapper",
  props:{
    group:{
      type:String,
      required:true
    },
    behavior:{
      type:String,
      required: false
    }
  },
  data(){
    return {
      fields:{},
      validationBag:{}
    }
  }
}
</script>

<style scoped>

</style>
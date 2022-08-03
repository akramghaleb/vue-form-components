<template>
  <form novalidate>
    <div class="container">
      <div class="row text-center justify-content-center">
        <div class="col-4">
          <slot
              :group="group"
              :fields="fields"
              :validation="validationBag"
          >
          </slot>
        </div>
      </div>
    </div>
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
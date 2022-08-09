<template>
  <div class="mb-3 text-start">
    <label for="full_Name" class="form-label">
      {{ label }} : {{ value }}</label>
    <textarea type="text"
           :id="identity"
           :name="name"
           :value="value"
           :maxlength="maxlength"
           :placeholder="placeholder"
           :autocomplete="autocomplete"
           @input="$emit('update:value', $event.target.value)"
              class="form-control"></textarea>
  </div>
</template>

<script>
export default {
  name: "textarea-input",
  props:{
    group: {
      type: String,
      required: false
    },
    label: {
      type: String,
      required: false
    },
    id : {
      type : String,
      required : false,
    },
    name:{
      type : String,
      required: true
    },
    value:{
      default:''
    },
    currentValue:{
      default:''
    },
    placeholder:{
      type : String,
      required : false
    },
    options: {
      type: [Array, Object, String],
      default: () => []
    },
    focus: {
      type: Boolean,
      default: false
    },
    maxlength: {
      type: String,
      required: false
    },
    autocomplete: {
      type: String,
      required: false
    },
    validation: {
      type: [Array, Object],
      default: () => []
    },
    visible: {
      type: Boolean,
      default: true
    },
    inputCssClass: {
      type: String,
      required: false
    },
    validationCssClass: {
      type: String,
      required: false
    },
    listen: {
      type: String,
      required: false
    },
    fire: {
      type: String,
      required: false
    }
  },
  data() {
    return {
      identity: this.id ? this.id : this.name,
      displayValidation: false,
      show: this.visible,
      val : ''
    }
  },
  emits: ['update:value'],
  mounted() {
    this.$emit('update:value', this.currentValue);
  }
}
</script>

<style scoped>

</style>
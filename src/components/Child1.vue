<template>
  <div>
    <h1>Child Component 1 - Event Based</h1>
    <b-input :value="value.fName" placeholder="First Name" @change="(event) => updateValue(event, 'fName')"/>
    <b-input :value="value.lName" placeholder="Last Name" @change="(event) => updateValue(event, 'lName')"/>
    <b-input :value="value.email" placeholder="Email" @change="(event) => updateValue(event, 'email')"/>
  </div>
</template>

<script>
export default {
  name: 'Parent',
  props: ['value'],
  methods: {
    updateValue(event, variable) {
      this.value[variable] = event
      this.$emit('input', this.value)
    }
  }
}
</script>

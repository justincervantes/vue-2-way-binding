<template>
  <div>
    <h1>Child Component 3 - Function and Event Based (TypeScript Compliant)</h1>
    <b-input :value="value.fName" placeholder="First Name" @change="updateFName"/>
    <b-input :value="value.lName" placeholder="Last Name" @change="updateLName"/>
    <b-input :value="value.email" placeholder="Email" @change="updateEmail"/>
  </div>
</template>

<script>
export default {
  name: 'Parent',
  props: ['value'],
  methods: {
    updateFName(event) {
      this.value['fName'] = event
      this.$emit('input', this.value)
    },
    updateLName(event) {
      this.value['lName'] = event
      this.$emit('input', this.value)
    },
    updateEmail(event) {
      this.value['email'] = event
      this.$emit('input', this.value)
    }
  }
}
</script>

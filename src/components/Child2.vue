<template>
  <div>
    <h1>Child Component 2 - Refs Based</h1>
    <b-input ref="fName" :value="value.fName" placeholder="First Name" @change="notifyParent"/>
    <b-input ref="lName" :value="value.lName" placeholder="Last Name" @change="notifyParent"/>
    <b-input ref="email" :value="value.email" placeholder="Email" @change="notifyParent"/>
  </div>
</template>

<script>
export default {
  name: 'Parent',
  props: ['value'],
  methods: {
    notifyParent() {
      this.$emit('input', {
        fName: this.$refs.fName.$refs.input.value,
        lName: this.$refs.lName.$refs.input.value,
        email: this.$refs.email.$refs.input.value,
      })
    }
  }
}
</script>

<template>
  <div>
    <h1>Parent Component</h1>
    <Child1 :value="childData1" @input="handleChildUpdate1"/>
    <Child2 :value="childData2" @input="handleChildUpdate2"/>
    <Child3 :value="childData3" @input="handleChildUpdate3"/>
  </div>
</template>

<script>
import Child1 from './Child1'
import Child2 from './Child2'
import Child3 from './Child3'

export default {
  components: {
    Child1,
    Child2,
    Child3
  },
  name: 'Parent',
  methods: {
    handleChildUpdate1 (args) {
      this.childData1 = args;
    },
    handleChildUpdate2 (args) {
      this.childData2 = args;
    },
    handleChildUpdate3 (args) {
      this.childData3 = args;
    }
  },
  data () {
    return {
      childData1: {
        fName: null,
        lName: null,
        email: null
      },
      childData2: {
        fName: null,
        lName: null,
        email: null
      },
      childData3: {
        fName: null,
        lName: null,
        email: null
      },
      childData4: {
        fName: null,
        lName: null,
        email: null
      }
    }
  }
}
</script>

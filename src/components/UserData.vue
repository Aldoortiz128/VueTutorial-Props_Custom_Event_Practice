<template>
  <section>
    <form @submit.prevent='submitData'>
    <!--Binding inputs to data-->
    <input type="text" placeholder="Your name" v-model='enteredName'/>
    <input type="text" placeholder="Your age" v-model="enteredAge"/>
    <button>Set User Data</button>
    </form>
  </section>
</template>

<script>
export default {
  //Listing Emit Events
  emits: ['set-data'],
  data() {
    return {
    enteredName: '',
    enteredAge: ''
    }
  },
  methods: {
    //Emit listener for form submit: identifier and input data parameters
    submitData(){
      this.$emit('set-data', this.enteredName, this.enteredAge)
    }
  },
};
</script>
<style>
</style>

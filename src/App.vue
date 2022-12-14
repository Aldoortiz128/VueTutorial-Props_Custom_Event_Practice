!<template>
  <div>
    <!--Props from ActiveUser being assigned the data below -->
    <active-user :username="user.name" :userage="user.age"></active-user>
    <!--Emit listener listen, then execute method -->
    <user-data @set-data="setUserData"></user-data>
  </div>
</template>
<script>
export default {
  //Manage all your data for your app here because you have access to all components
  data() {
    return {
        //User Object
        user: {
            name: "Aldo Ortiz",
            age: 25
        }
    }
  },
  methods: {
    //Emit listener data from UserData assigning data to our user object above
    setUserData(username, userage) {
        this.user = {
        name: username,
        //Converts string to a number
        age: +userage
        }
    }
  },
};
</script>
<style>
html {
  font-family: sans-serif;
}
section {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid #ccc;
  padding: 1rem;
}
</style>


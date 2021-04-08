<template>
  <div class="login">
    <h1>This is a login page</h1>
    <v-text-field
      label="Username"
      v-model="input.username"
      clearable>
    </v-text-field>
    <v-text-field
      label="Password"
      v-model="input.password"
      clearable>
    </v-text-field>
    <p>down here we show these things</p>
    <p>{{input.username}}</p>
    <p>{{input.password}}</p>
    <v-btn
      color=red
      v-on:click="login"
    >LOGIN</v-btn>
  </div>
</template>

<script>
const axios = require('axios')

export default {
  name: 'UserLogin',

  data: () => ({
    apiUrl: process.env.VUE_APP_ROOT_API,
    input: {
      username: "",
      password: ""
    }
  }),
  methods: {
    login: function() {
      console.log(this.input.password)
      axios.post(`${this.apiUrl}/auth/signin`,{
        username: this.input.username,
        password: this.input.password
      })
      .then(function(response) {
        console.log(response)
      })
    }
  }
};
</script>

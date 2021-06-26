<template>
  <div class="login">
    <h1>This is a login page</h1>
    <v-text-field
      label="Username"
      v-model="input.username"
      clearable>
    </v-text-field>
    <v-text-field
      label="password"
      v-model="input.password"
      clearable
      >
    </v-text-field>
    <p>down here we show these things</p>
    <p>user {{input.username}}</p>
    <p>pass{{input.password}}</p>
    <p>token {{accessToken}}</p>

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
      username: "chris23",
      password: "123456",
    },
    accessToken: ""
  }),
  methods: {
    login: function() {
      console.log(this.input.password)
      axios.post(`${this.apiUrl}/auth/signin`,{
        username: this.input.username,
        password: this.input.password
      })
      .then((response) => {
        console.log(response)
        this.accessToken = response.data.accessToken
      })
    }
  }
};
</script>

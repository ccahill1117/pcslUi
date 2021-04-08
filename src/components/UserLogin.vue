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
export default {
  name: 'UserLogin',

  data: () => ({
    input: {
      username: "",
      password: ""
    }
  }),
  methods: {
    login: function() {
      console.log(this.input.password)
    }
  }
};
</script>

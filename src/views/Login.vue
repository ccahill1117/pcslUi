<template>
  <div class="login">
    <h1>This is a login page</h1>
    <v-form @submit="login">
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
        type="submit"
      >LOGIN</v-btn>
    </v-form>
  </div>
</template>

<script>
export default {
  name: 'Login',

  data: () => ({
    apiUrl: process.env.VUE_APP_ROOT_API,
    input: {
      username: "",
      password: ""
    }
  }),
  methods: () => ({
    login: function() {
      console.log(this.input.username)
    }
  })
};
</script>

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
  </div>
</template>

<script>
export default {
  name: 'Login',

  data: () => ({
    input: {
      username: "",
      password: ""
    }
  }),
};
</script>

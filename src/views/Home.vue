<template>
  <div class="home">
    <h2>environment variable test {{apiUrl}}</h2>
    <UserLogin></UserLogin>
  </div>
</template>

<script>

// @ is an alias to /src
import UserLogin from '@/components/UserLogin.vue'


export default {
  name: 'home',
  data: function () {
    return {
      apiUrl: process.env.VUE_APP_ROOT_API
    }
  },
  components: {
    'UserLogin': UserLogin
  }
}
</script>

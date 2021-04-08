<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h2>environment variable test {{apiUrl}}</h2>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  data: function () {
    return {
      apiUrl: process.env.VUE_APP_ROOT_API
    }
  },
  components: {

  }
}
</script>

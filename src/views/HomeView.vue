<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <navigator />
  </div>
</template>

<script>
// @ is an alias to /src
import navigator from '../components/navigator.vue'

export default {
  name: 'HomeView',
  components: {
    navigator
  }
}
</script>

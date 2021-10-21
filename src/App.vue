<template>
  <div>
    <Login />
  </div>
</template>

<script>
import Login from "./components/Login.vue";
export default {
  name: 'App',
  components: {
    Login
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

#app {
  font-family: 'Inter', 'sans-serif';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.text__color--dark {
  color: rgba(33,35,41, 0.9);
}
.bg__color--dark {
  background-color: rgba(33,35,41, 0.9);
}

</style>

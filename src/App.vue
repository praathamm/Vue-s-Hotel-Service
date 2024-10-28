<template>

<SignUp/>
</template>

<script>
import SignUp from './components/SignUp.vue';
import Cat from './components/Cat.vue'; 



export default {
  name: 'App',
  components: {
    SignUp,
    Cat
  }
}

</script>
<style>
html, body, #app {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}
</style>

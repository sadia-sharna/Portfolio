<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Sadia Tasnim Portfolio"/>
    <About v-bind:userdata="userdata"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import About from '@/views/About.vue';

export default {
  name: 'Home',
  components: {
    HelloWorld,
    About
  },
  data() {
      return {
          userdata: {
            name: 'Sadia',
            sex: 'Female',
            age: 23
          },

      }
  },
}
</script>

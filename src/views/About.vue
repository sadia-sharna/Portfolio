<template>
  <div class="about">
    <h1>This is an about page</h1>
      <p>My Name is {{userdata.name}}</p>
    <p>My age is {{userdata.age}}</p>
  
  </div>
</template>
<script>
export default {
  name: 'About',
  props: {
    userdata: Object
  }

}
</script>

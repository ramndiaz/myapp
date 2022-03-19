<template>
  <div class="user">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'User',
  data () {
    return {
      msg: 'User Component'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.user{
  background-color: aqua;
}
</style>

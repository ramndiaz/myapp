<template>
  <div class="test">
    <p>{{ msg }}</p>
    <p>{{ user.name }}</p>
    <p>{{ user }}</p>
    <ul>
      <li v-for="task in tasks" :key="task.name">
        {{ task }}
      </li>
    </ul>
    <input type="text" name="" v-on:keyup.enter="function2">
    <input type="text" name="" v-model="user.name">
    <input type="text" name="" v-model="user.age">
    <button type="button" v-on:click="function1(user.name)">send</button>
    <hr>
  </div>
</template>

<script>
export default {
  name: 'Test',
  data () {
    return {
      msg: 'Test Component',
      user: {
        name: 'pedro',
        age: 29
      },
      myHtml: '<p>test paragraf</p>',
      tasks: [
        {name: 'eat'},
        {name: 'dream'},
        {name: 'drink'},
        {name: 'talk'},
        {name: 'play'}
      ]
    }
  },
  methods:{
      function1(name){
        alert("klk " + name)
      },
      function2(e){
        console.log(e.target.value)
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.test{
  background-color: aqua;
}
</style>

<template>
  <div class="test">
    <h1>{{ msg }}</h1>
    <h1>{{ user.name }}</h1>
    <h1>{{ user }}</h1>
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
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

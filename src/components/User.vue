<template>
  <div class="user">
    <p>{{ msg }}</p>
    <table>
      <tbody>
        <tr v-for="todo in todos" :key="todo.id">
          <td>user id: {{todo.userId}}</td>
          <td>id: {{todo.id}}</td>
          <td>title: {{todo.title}}</td>
          <td>complete: {{todo.completed}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
//axios primero debe instalarse con npm
import axios from 'axios'
export default {
  name: 'User',
  data () {
    return {
      msg: 'User Component',
      todos:null
    }
  },
  mounted(){
    //mounted metodo reservado de vue para cuando el componente se monta en el DOM
    //console.log('prueba desde mounted')
    this.getTodos();
  },
  methods:{
    getTodos(){
      //console.log('esto es getTodos')
      axios
        .get('https://jsonplaceholder.typicode.com/todos')
        //endpoint de prueba con datos al azar
        .then( response => {
          //console.log(response)
          this.todos=response.data
        })
        .catch( e=> console.log(e))
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

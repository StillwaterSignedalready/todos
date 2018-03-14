<template>
  <div>
    <input type="text" v-model="msg" v-on:keypress="bark">
    <ul v-for="todo in todos">
      <li>{{todo}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      msg: 'iieiei',
      todos: []
    }
  },
  methods: {
    bark(event){
      if(event.key == 'Enter'){
        this.$data.todos.push(this.$data.msg);
        console.log(this.$data.todos);
        this.$data.msg = '';
      }
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

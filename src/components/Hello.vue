<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input class="input" type="text" id="content" ref="input1"> <input class="button" type="submit" @click="doSomething">
    <p v-for="item in todo">{{item}}</p>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return  {
    msg: 'ToDo-List',
    todo: ['666'],
    }
  }, 
  methods: {
    doSomething: function() {
      var inputText = this.$refs.input1.value;
      this.todo.push(inputText);
    }
  },
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

input.input {
  height: 40px;
  width: 600px;
  border-width: 1px;
  border-radius: 4px;
  line-height: 40px;
  outline: none;
}

input.button {
  height: 40px;
  width: 150px;
  border: none;
  border-radius: 4px;
  background-color:   #2ecc71;
}
</style>

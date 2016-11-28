<template>
  <div class="container">
    <div id="app">
      <!-- <pre>{{ $data }}</pre> -->
      <div class="row">
        <div class="col-md-8 col-md-offset-2">
          <h2>Awesome Todo</h2>
          <form class="form-horizontal" action="">

            <div class="input-group">
             <input type="text" class="form-control" v-model="todo">
             <span class="input-group-btn">
                  <button class="btn btn-success" type="button">+</button>
             </span>
          </div>
          </form>

          <ul class="list-group">
            <li class="list-group-item" v-for="(todo, index) in todoList">
              {{ todo.task }}
              <button class="btn btn-danger btn-xs pull-right">X</button>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      todoList: [
        { id: 1, task: 'Get Paid'},
        { id: 2, task: 'Take mom out for a treat.'}
      ],
      newTodoItem: {id: null, task: ''}
    }
  }
}


</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
ul.list-group {
    margin-top: 15px;
}

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

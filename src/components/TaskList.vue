<template lang="html">
  <!-- <p>Hello from TaskList.</p> -->
  <ul class="list-group">
    <li class="list-group-item text-left" v-for="todo in taskList">
      {{ todo.title }}
      <button class="btn btn-danger btn-xs pull-right">X</button>
    </li>
    <!-- <li class="list-group-item">Propose to bae <button type="button" name="button" class="btn btn-danger  btn-xs pull-right">x</button></li>
    <li class="list-group-item">Get lunch <button type="button" name="button" class="btn btn-danger btn-xs pull-right">x</button></li> -->
    <!-- <li class="list-group-item" v-for="(todo, index) in todoList">{{ todo.task }}<button type="button" name="button" class="btn btn-danger btn-xs pull-right">x</button></li> -->
  </ul>
</template>

<script>
export default {
  data () {
    return {
      taskList: [
        {id: 1, title: 'Go for NPP national rally', dueDate:""},
        {id: 2, title:'Go to Silverbird with bae'}
      ],
      newTask: {id: null, title:''}
    }
  }
}
</script>

<style lang="css">
</style>

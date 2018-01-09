<template>
  <div id="app" class="container">
    <div class="todo-wrapper">
      <todo-header></todo-header>
      <div class="todo-content">
        <todo-report></todo-report>
        <todo-list :collection="liststate.items"></todo-list>
      </div>
    </div>
  </div>
</template>

<script>
import ListStore from './data/store.js';
import TodoHeader from './components/TodoHeader.vue';
import TodoReport from './components/TodoReport.vue';
import TodoList from './components/TodoList.vue';

export default {
  data() {
    return {
      liststate: ListStore.state
    }
  },
  components: {
    TodoHeader,
    TodoReport,
     TodoList
  }
}
</script>

<style lang="stylus">
@import "../styl/style.styl"
</style>

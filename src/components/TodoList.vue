<template>
    <div class="todo-list">
        <todo-listItem 
            v-for="todo in todos" 
            :key="todo.id" 
            :todo-item="todo"
            @change-state="todo.completed = $event.target.checked">
        </todo-listItem>
    </div>
</template>

<script>
import TodoListItem from '@/components/TodoListItem.vue';

export default {
    name: "TodoList",
    components: { TodoListItem },
    props: ["todos"]
}
</script>

<style scoped>
.todo-list {
  display: grid;
  row-gap: 14px;
}
</style>
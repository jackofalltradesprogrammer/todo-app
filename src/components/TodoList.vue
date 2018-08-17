/* eslint-disable */
<template>
    <div>
        <p>Complete Tasts: {{todos.filter(todo => {return todo.done == true}).length}}</p>
        <p>Pending Tasts: {{todos.filter(todo => {return todo.done == false}).length}}</p>
        <!-- We are now passing data to the child component "Todo" to render the todo list -->
        <todo v-on:delete-todo="deleteTodo" v-for="todo in todos" :key="todo.null" v-bind:todo="todo"></todo>
        
    </div>
</template>

<script type = "text/javascript" >
import Todo from './Todo';
export default {
    props:['todos'],
    components: {
        Todo,
    },
    methods: {
        deleteTodo(todo){
            const todoIndex = this.todos.indexOf(todo);
            this.todos.splice(todoIndex,1); 
        },
    },
};
</script>

<style>

</style>

/* eslint-disable */
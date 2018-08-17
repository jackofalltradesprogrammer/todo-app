/* eslint-disable */
<template>
    <div>
        <p>Complete Tasts: {{todos.filter(todo => {return todo.done == true}).length}}</p>
        <p>Pending Tasts: {{todos.filter(todo => {return todo.done == false}).length}}</p>
        
    </div>
</template>

<script type = "text/javascript" >

export default {
    props:['todos'],
};
</script>

<style>

</style>

/* eslint-disable */
<template>
    <div class="todo-item" v-bind:class="{'is-complete':todo.completed} ">
        <p> 
            <input type="checkbox" v-on:change="markComplete">
            {{todo.title}} 
            <button @click="$emit('del-todo', todo.id)" class="del">X</button>
        </p>
    </div>
</template>

<script>
export default {
    name: "TodoItem",
    props: ["todo"],
    methods: {
        markComplete(){
            this.todo.completed = !this.todo.completed;
        }
    }
}
</script>

<style scoped>
    .todo-item
    {
        background: #f4f4f4;
        padding: 10px;
        border: 1px dotted #333;
    }

    .is-complete
    {
        text-decoration: line-through;
    }

    .del
    {
        background: #f73a3a;
        color: #fff;
        border: none;
        padding: 5px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
    }
</style>
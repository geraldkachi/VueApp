<template>
    <div class="todo-item" v-bind:class="{'is-completed':todo.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{todo.title}}
            <button @click="$emit('del-todo', todo.id)" type="button" class="del">X</button>
        </p>
    </div>
</template>

<script>
export default {
    name: "TodoItem",
    props: ["todo"],
    method: {
        markComplete() {
            console.log(123);
            // this.todo.completed = !this.todo.completed;
        }
    }
}
</script>


<style scoped>
    .todo-item {
        background: #ff4f4f;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
    }

    .is-completed {
        text-decoration: line-through;
        }
    .del {
        background: #ff0000;
        color: #fff;
        border: none;
        padding: 5px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
    }
</style>
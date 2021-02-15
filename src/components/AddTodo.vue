<template>
    <div>
        <form @submit="addTodo">
            <input type="text" name='title' placeholder="Add Todo...">
            <input type="submit" value='Submit' class="btn">
        </form>
    </div>
</template>

<script>
export default {
    name: "AddTodo",
    data() {
        return {
            title: ''
        }
    },
    method: {
        addTodo() {
            const newTodo = {
                
            }
        }
    }
}
</script>

<style scoped>

    form {
        display: flex;
    }
    input[type="text"] {
        flex: 10;
        padding: 5px;
    } 
    .btn {
        flex: 2;
    }
</style>
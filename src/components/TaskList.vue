<template>
    <div class="list-container">
        <ul class="list" :key="task" v-for="task in tasks">
            <li class="item">{{ task.title }}<button class="delete-btn" v-on:click="deleteItem(task.id)">Delete</button></li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: {
            tasks: Array
        },
        methods: {
            deleteItem(id) {
                this.$emit('gitridof', id)
        }
    }
    }
</script>

<style scoped>
    .item {
        list-style: none;
        border: 2px solid greenyellow;
        padding: 20px;
    }

    .list {
        display: flex;
        flex-direction: column;
    }

    .list-container {
        width: 455px;
    }

    .delete-btn {
        position: relative;
        left: 100px;
        cursor: pointer;
        text-transform: uppercase;
        font-weight: bold;
        border: none;
        padding: 10px;
        border-radius: 5px;
        background:red;
        color: white;
    }
</style>
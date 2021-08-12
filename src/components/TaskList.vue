<template>
    <div class="list-container">
        <ul class="list" :key="task" v-for="task in tasks">
            <li class="item">{{ task }}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: {
            tasks: Array
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
</style>
<template>
    <div>
        <ul class="list" :key="task" v-for="task in tasks">
            <li class="item">{{ task }}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: {
            tasks: []
        }
    }
</script>

<style scoped>
    .item {
        list-style: none;
        border: 2px solid greenyellow;
    }

    .list {
        display: flex;
        flex-direction: column;
    }
</style>
<template>
    <div>
        <form @submit.prevent="handleTaskAdd">
            <input type="text" placeholder="Enter in task..." v-model="value"/>
            <button>Add Task</button>
        </form>
        <TaskList v-bind:tasks="this.task"/>
    </div>
</template>
    
<script>
    import TaskList from './TaskList.vue';

    export default {
        name: "TaskForm",
        data() {
            return {
                value: "",
                task: []
            }
        },
        methods: {
            handleTaskAdd() {
                this.task.push(this.value)
                this.value = ""
            },
        },
        components: {
            TaskList
        }

    }
</script>

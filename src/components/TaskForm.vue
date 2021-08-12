<template>
    <div>
        <form @submit.prevent="handleTaskAdd" >
            <input type="text" placeholder="Enter in task..." v-model="value"/>
            <button>Add Task</button>
        </form>
        <TaskList v-bind:tasks="this.tasked" v-on:gitridof="deleteTask($event)"/>
    </div>
</template>
    
<script>
    import TaskList from './TaskList.vue';

    export default {
        name: "TaskForm",
        data() {
            return {
                value: "",
                tasked: [],
            }
        },
        methods: {
            handleTaskAdd() {
                let task = {
                    title: this.value,
                    id: Math.floor(Math.random() * 900000)
                }

                //console.log(task)
                this.tasked = [...this.tasked, task]
                this.value = ""
            },
            deleteTask(ids) {
                this.tasked = this.tasked.filter(task => task.id !== ids)
            }
        },
        components: {
            TaskList
        },
        emits: ['deleted']

    }
</script>

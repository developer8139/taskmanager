<template>
    <div>
        <form @submit.prevent="handleTaskAdd()">
            <input type="text" placeholder="Enter in task..."  @change="value"/>
            <button>Add Task</button>
        </form>
    </div>
</template>

<script>
    export default {
        name: "TaskForm",
        data() {
            return {
                value: ""
            }
        },
        methods: {
            handleTaskAdd() {
                console.log(this.value)
            }
        }

    }
</script>

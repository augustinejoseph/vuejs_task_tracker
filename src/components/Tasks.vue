<template>
    <div v-for=" task in tasks" :key="task.id">
        <Task :task='task' />
    </div>
</template>

<script>
import Task from './Task.vue'
export default {
    name: 'TasksComp',
    props: {
        tasks: {
            type: Array,
        }
    },
    components: {
        Task
    },
}
</script>
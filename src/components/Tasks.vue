<template>
    <div v-for=" task in tasks" :key="task.id">
        <h3>{{ task?.name }}</h3>
    </div>
</template>

<script>
export default {
    name: 'TasksComp',
    props: {
        tasks: {
            type: Array,
            required: true
        }
    }
}
</script>
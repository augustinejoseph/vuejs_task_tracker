<template>
    <div>
        <h1>{{ title }}</h1>
        <Button text="Add Task!!!" color="green" />
    </div>
</template>

<script>
import Button from './Button.vue';
export default {
    name: 'HeaderMain',
    props: { 'title': String },
    components: {
        Button
    },
}
</script>

<style scoped>
header {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;
}
</style>
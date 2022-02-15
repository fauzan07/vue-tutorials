<template>
    <div class="child1-com">
        <h1>Child 1 Component</h1>
        <Child2/>
    </div>
</template>

<script>
import Child2 from './Child2.vue';
export default {
    components: { Child2 },
    name : "Child1"
}
</script>

<style>
.child2-com{
    background-color: aquamarine;
    padding: 10px;
}
</style>
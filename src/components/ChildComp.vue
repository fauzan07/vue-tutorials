<template>
    <div class="ChildComp">
        <!-- <h1>Child Component</h1> -->
        <button @click="updateTitle">Update parent title</button>
    </div>
</template>

<script>
export default {
    name : "ChildComp",
    methods : {
        updateTitle(){
            this.$emit('changeTitle' , 'parent updated')
        }
    }
}
</script>

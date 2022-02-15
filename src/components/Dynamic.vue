<template>
    <div>
        <h3>{{name}}</h3>
        <h3>{{10 + 10}}</h3>
        <h3>{{a + b}}</h3>
        <h3>{{ok ? "yes show" : "Not show"}}</h3>
        <p v-html="appentHtml"></p>
        <button v-bind:disabled="disablebtn" v-on:click="updateText">Click Me</button>
    </div>
</template>

<script>
export default {
    name : "Dynamic",
    methods : {
        updateText(){
            this.name="max"
        }
    },
    data(){
        return {
            name : "anil",
            a: 10,
            b: 20,
            ok : true,
            appentHtml : '<span>Append Html tag</span>',
            disablebtn : true
        }
    },
}
</script>
<template>
<div>
    <div>
        <h1 v-size>Custom Directive</h1>
        <h1 v-size="'small'">Custom Directive</h1>
        <h1 v-size="'big'">Custom Directive</h1>
    </div>
</div>
</template>

<script>

export default {
    name : "CustomDirective",
    data(){
        return {
        }
    },
}
</script>
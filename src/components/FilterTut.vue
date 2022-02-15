<template>
    <div>
        <h3>{{name | Ucase}}</h3>
    </div>
</template>

<script>
export default {
    name : "FilterTut",

    data(){
        return {
            name : "vue filter tut"
        }
    }
}
</script>
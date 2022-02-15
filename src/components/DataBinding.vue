<template>
    <div>
        <h1 style="white-space:pre-line">{{message}}</h1>
        <!-- <input type="text" v-model="message"/> -->
        <textarea type="text" v-model="message"></textarea>
    </div>
</template>

<script>
export default {
    name : "DataBinding",
    data(){
        return {
            message : 'hi'
        }
    }
}
</script>
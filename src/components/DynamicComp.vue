<template>
<div>
    <div>
        <h1>Dynamic Component</h1>
        <!-- <SignIn/>
        <SignUp/> -->
        <component v-bind:is="cmp"></component>
        <!-- <button @click="updateCmp('signin')">Sign In</button>
        <button @click="updateCmp('signup')">Sign In</button> -->
        <!-- also -->
        <button @click="cmp='signin'">Sign In</button>
        <button @click="cmp='signup'">Sign In</button>
    </div>
</div>
</template>

<script>
import SignIn from './DynamicComp/SignIn.vue'
import SignUp from './DynamicComp/SignUp.vue'

export default {
    name : "DynamicComp",
    components : {
        'signin' : SignIn,
        'signup' : SignUp
    },
    data(){
        return {
            cmp : 'signin'
        }
    },
    // methods : {
    //     updateCmp(item){
    //         this.cmp=item
    //     }
    // },
}
</script>
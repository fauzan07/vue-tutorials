<template>
    <div>
        <div v-if="display">
        <h1 id="demo">{{name}}</h1>
        </div>
        <button @click="toggle">toggle</button>
    </div>
</template>

<script>
export default {
    name : "LifeCycle",
    data(){
        return{
            name : "life cycle before create and created",
            display : true
        }
    },
    methods : {
        toggle(){
            this.display = !this.display
        }
    },
    created(){
        // this.name = 'i am form created'
        console.log('hello created',this.name);
    },
    beforeCreate(){
        // this.name = 'i am from before create'
        console.log('hello beforecreated',this.name);//name will display first than component created
    },
    beforeMount(){
        console.log('hello beforeMount',document.getElementById('demo'));
    },
    mounted(){
        console.log('hello mounted',document.getElementById('demo'));//used to modify html dom element
    },
    beforeDestroy(){
        console.log("hello before distroy")
    },
    destroyed(){
        console.log("hello distroy")
    }
}
</script>

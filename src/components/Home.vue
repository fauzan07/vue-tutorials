<template>
    <div>
        <h1>hello i am from Home Component</h1>
        <h1 v-bind:style="{color : 'red'}">hello i am {{msg}}</h1>
        <button @click="hello('alert called')">Call Hello Function</button>
        <h1 v-if="show">Conditional rendering in vue</h1>
        <h1 v-else>Conditional rendering in else condition</h1>
        <button v-on:click="display">toggle</button>
        <table border="1px">
            <tr>
                <th>Id</th>
                <th>Name</th>
                <th>Email</th>
            </tr>
            <tr v-for="item in users" :key="item.id">
                <td>{{item.id}}</td>
                <td>{{item.name}}</td>
                <td>{{item.email}}</td>
            </tr>
        </table>
        <Child1/>
    </div>
</template>

<script>
import Child1 from './Child1.vue';
export default {
  components: { Child1 },
    name : "Home",
    // props : {
    //     msg : String
    // },
     props : [
         'msg'
     ],
    methods : {
        hello(data){
            console.log("hello function called");
            alert(data)
        },
        display(){
            this.show=!this.show
        }
    },
    data(){
        return {
            show:true,
            users : [
                {id:1,name:"paul",email:"paul@gmail.com"},
                {id:2,name:"sid",email:"sid@gmail.com"},
                {id:3,name:"max",email:"max@gmail.com"}
            ]
        }
    },
}
</script>
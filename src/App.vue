<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <Home msg="msg from Home"/> -->
    <!-- <Dynamic/> -->
    <!-- <DataBinding/> -->
    <!-- <PropsBinding name="bind name via props" v-bind:users="users"/> -->
    <!-- <h1>{{title}}</h1> -->
    <!-- <ChildComp v-on:changeTitle="updateTitle($event)"/> -->
    <!-- <FormBinding/> -->
    <!-- <FilterTut/> -->
    <!-- <LifeCycle/> -->
    <!-- <AxiosTuts/> -->
    <BootstrapTuts/>
  </div>
</template>

<script>
  import BootstrapTuts from './components/BootstrapTuts.vue'
// import AxiosTuts from './components/AxiosTuts.vue'
// import LifeCycle from './components/LifeCycle.vue'
// import FilterTut from './components/FilterTut.vue'
// import FormBinding from './components/FormBinding.vue'
// import ChildComp from './components/ChildComp.vue';
// import HelloWorld from './components/HelloWorld.vue';
// import Home from './components/Home.vue';
// import Dynamic from './components/Dynamic.vue';
// import DataBinding from './components/DataBinding.vue';
// import PropsBinding from './components/PropsBinding.vue';



export default {
  name: 'App',
  components: {
    BootstrapTuts
    // AxiosTuts
    // LifeCycle
    // FilterTut
    // FormBinding
    // HelloWorld,
    // Home,
    // ChildComp
    // Dynamic
    //  DataBinding
    // PropsBinding
  },
  data(){
    return{
      // users : [
      //   {id:1,name:"paul",email:"paul@gmail.com"},
      //   {id:2,name:"sid",email:"sid@gmail.com"},
      //   {id:3,name:"max",email:"max@gmail.com"}
      //   ],

        // title:"child to parent prop called"
    }
  },
  // methods : {
  //   updateTitle(title){
  //     this.title=title
  //   }
  // }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

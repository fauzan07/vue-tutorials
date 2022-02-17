<template>
<div>
    <div>
        <h1>Delete Post from json</h1>
            <table border="1px">
            <tr>
                <th>Id</th>
                <th>Title</th>
                <th>Author</th>
                <th>Action</th>
            </tr>
            <tr v-for="item in posts" :key="item.id">
                <td>{{item.id}}</td>
                <td>{{item.title}}</td>
                <td>{{item.author}}</td>
                <td><button v-on:click="deletePosts(item.id)">Delete Posts</button></td>
            </tr>
        </table>
    </div>
</div>
</template>

<script>
import Vue from 'vue';
import VueAxios from 'vue-axios';
import axios from 'axios';
Vue.use(VueAxios,axios)
export default {
    name : "PostDataDelete",
    data(){
        return {
         posts : null
        }
    },
    methods : {
      getPosts(){
          Vue.axios.get('http://localhost:3000/posts')
            .then(resp => {
            this.posts = resp.data
            console.log(resp.data);
        })
      },
      deletePosts(id){
          Vue.axios.delete('http://localhost:3000/posts/'+id)
            .then(resp => {
                this.getPosts()
                console.log(resp);

        })
      }
    },
    mounted(){
        this.getPosts()
    }
}
</script>
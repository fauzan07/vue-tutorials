<template>
<div>
    <div>
        <h1>Add Post to json</h1>
         <form @submit="onSubmit">
            <label for="title">Title</label><br/>
            <input type="text" name="title" id="title" v-model="posts.title"><br/><br/>
            <label for="author">Author</label><br/>
            <input type="text" name="author" id="author" v-model="posts.author"><br/><br/>
            <button type="submit">Sumbit</button>

        </form>
    </div>
    <!-- <div>
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
                <td><button @click="deletePosts(item.id)">Delete Posts</button></td>
            </tr>
        </table>
    </div> -->
</div>
</template>

<script>
import Vue from 'vue';
import VueAxios from 'vue-axios';
import axios from 'axios';
Vue.use(VueAxios,axios)
export default {
    name : "PostData",
    data(){
        return {
         posts : {
             title : null,
             author : null
         }
        }
    },
    methods : {
      onSubmit(e){
            e.preventDefault();
             Vue.axios.post('http://localhost:3000/posts', this.posts)
                .then(resp => {
                    console.log(resp);
                })
      },
    //   getposts(){
    //       Vue.axios.get('http://localhost:3000/posts')
    //         .then(resp => {
    //         this.posts = resp.data
    //         console.log(resp.data);
    //     })
    //   },
    //   deleteposts(id){
    //       Vue.axios.delete('http://localhost:3000/posts/'+id)
    //         .then(resp => {
    //             this.getposts()
    //             console.log(resp);

    //     })
    //   }
    },
    // mounted(){
    //     this.getposts()
    // }
}
</script>
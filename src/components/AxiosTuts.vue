<template>
    <div>
        <h1>Employee list</h1>
         <table border="1px">
            <tr>
                <th>Id</th>
                <th>Name</th>
                <th>Age</th>
                <th>Salary</th>
            </tr>
            <tr v-for="item in list" :key="item.id">
                <td>{{item.id}}</td>
                <td>{{item.employee_name}}</td>
                <td>{{item.employee_age}}</td>
                <td>{{item.employee_salary}}</td>
            </tr>
        </table>
    </div>
</template>

<script>
import Vue from 'vue';
import VueAxios from 'vue-axios';
import axios from 'axios';
Vue.use(VueAxios,axios)
export default {
    name : "AxiosTuts",
    data(){
        return {
            list : undefined
        }
    },
    mounted(){
        Vue.axios.get('http://dummy.restapiexample.com/api/v1/employees')
        .then(resp => {
            this.list = resp.data.data
            console.log(resp.data.data);
        })
    }
}
</script>
<template>
    <div>
        <h1>{{name}}</h1>
         <table border="1px">
            <tr>
                <th>Id</th>
                <th>Name</th>
                <th>Email</th>
            </tr>
            <tr v-for="user in users" :key="user.id">
                <td>{{user.id}}</td>
                <td>{{user.name}}</td>
                <td>{{user.email}}</td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {
    name : "PropsBinding",
    props : ['name','users']
}
</script>

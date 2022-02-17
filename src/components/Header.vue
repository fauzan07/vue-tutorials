<template>
    <div>
        <ul>
            <li><router-link to="/">Home</router-link></li>
            <li><router-link to="/post">Posts</router-link></li>
        </ul>
        <router-view></router-view>
    </div>
</template>

<script>
export default {
    name : "Header",
}
</script>
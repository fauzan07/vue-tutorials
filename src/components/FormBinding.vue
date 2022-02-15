<template>
    <div class="Formbinding">
        <h1>Form Binding</h1>
        <p v-if="error.length">
            <b>Please correct the following error</b>
            <ul>
                <li v-for="e in error" :key="e.id">
                    {{e}}
                </li>
            </ul>
        </p>
        <form @submit="onSubmit">
            <label for="cricket">Username</label><br/>
            <input type="text" name="email" id="email" v-model="getformdata.userName"><br/><br/>
            <label for="cricket">Password</label><br/>
            <input type="text" name="password" id="password" v-model="getformdata.passWord"><br/><br/>
            <input type="checkbox" name="cricket" id="cricket" value="cricket" v-model="getformdata.games"><label for="cricket">cricket</label><br/><br/>
            <input type="checkbox" name="football" id="football" value="football" v-model="getformdata.games"><label for="football">football</label><br/><br/>
            <input type="checkbox" name="backetball" id="basketball" value="basketball" v-model="getformdata.games"><label for="basketball">basketball</label><br/><br/>
            <input type="radio" name="male" id="male" value="male" v-model="getformdata.gender"><label for="male">male</label><input type="radio" name="female" id="female" value="female" v-model="getformdata.gender"><label for="female">female</label><br/><br/>
            <!-- <button @click="userDetails">Sumbit</button> -->
            <button type="submit">Sumbit</button>

        </form>
    </div>
</template>

<script>
export default {
    name : "Formbinding",
    data(){
        return{
            error : [],
            getformdata : {
                userName : null,
                passWord : null,
                games : [],
                gender : null
            }
        }
    },
    methods : {
        // userDetails(){
        //     console.log(this.getformdata);//get all data
        //     console.log(this.getformdata.userName);//get perticular data
        // }
        onSubmit(e){
            this.error = [];
            e.preventDefault();
            if(this.getformdata.userName && this.getformdata.passWord && this.getformdata.gender){
                console.log("no error");
            }
            if(!this.getformdata.userName){
                this.error.push("username is required")
            }
            if(!this.getformdata.passWord){
                this.error.push("password is required")
            }
            if(!this.getformdata.gender){
                this.error.push("gender is required")
            }
            console.log(this.error);
            console.log(this.getformdata);//get all data
        }
    }
}
</script>

<template>
    <div class="form">
    <form  v-on:submit="login">
    <!-- <label class="text">Username : </label> -->
    <input  type = "text" class="text" placeholder="Enter Username"/>
    <br>

    <!-- <label class="text">Password : </label> -->
    <input type="password" class="text" placeholder="Enter Password"/>
    <br>

    <input class ="submit" type="submit" value="Login" />    
  </form>

    </div>
   
  
</template>

<script>
    import router from "../router"    
    import axios from "axios"    
    export default {    
    name: "Login",    
    methods: {    
         login: (e) => {
            e.preventDefault()    
            let username = "username"   
            let password = "password"    
            let login = () => {    
            let data = {    
                username: username,    
                password: password    
            }    
            axios.post("/api/login", data)    
            .then((response) => {    
                console.log("Logged in")
                router.push("/dashboard")    
            })    
            .catch((errors) => {    
                console.log("Cannot log in")    
                    })    
                }    
            login()    
            }    
        }    
    }
</script>

<style>
.text{
    height:25px;

    border: 10px;
    margin-left:60px;
    margin-top: 10px;
    border-color: rgb(41, 36, 36);
    background-color: rgb(239, 241, 241);
   


}

.submit{
    width:80px;
    height:25px;
    margin-left:100px;
    margin-top: 10px;
    border-radius: 10px;
    border: 30px;
    background-color: rgb(190, 197, 197);
   
}

.form{
    width:300px;
    height:200px;

}
</style>

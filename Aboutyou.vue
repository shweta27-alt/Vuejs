<template>
    <div class="container">
        <h1 class="aboutyou">About You</h1>
        <form v-on:submit="about" @submit.prevent="getFormValues">
            <div class="name">
                 <lable>First Name</lable>
                 <div> <input type="text"  v-model="exampleInputFirstname"   /></div>
                
            </div>

            <div class="name">
                <label>Last Name</label>
                <div> <input type="text" v-model="exampleInputlastname"/></div>
               
            </div>

            <div class="name">
                <label>Pin Code</label>
                <div><input type="text" v-model="exampleInputpincode"/></div>
       
            </div>

            <div class="submit-button" >
                <button type="submit" v-on:click="login"> Submit</button>
            </div>
            
        </form>
    </div>
    
</template>

<script>
export default{
    methods:{
        login(){
           console.log(this.login_data)
        }
    },

    data(){
        return{
            login_data:{
              firstname:null,
              lastname:null,
              pincode:null
            }
        }
    }
}

</script>

<style>

.container{
    height:300px;
    width:200px;
    background-color: rgb(237, 235, 235);
}
.name{
    margin-top:10px;
    margin-left:10px;
}

.submit-button{
   margin-top:10px;
   margin-left:40px;
    
}

.aboutyou{
    margin-left:10px;
    font-family: Arial, Helvetica, sans-serif;
}



</style>

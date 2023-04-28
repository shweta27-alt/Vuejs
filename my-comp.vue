<template>
    <div>
        <button v-on:click="Clickme"> Button</button>
        <h1 v-bind:class="status">{{ status }}</h1>

        <input v-model="mymodel" type="text"  ref="mohit">

        <br>

        <input v-bind:value="mymodel" @input="newtext" type="text">

        <div> {{ hello }} <br> {{ msg }}</div>
    </div>
    
</template>

<script>
export default{
    data(){
        return{
            status:"Shweta",
            mymodel:"write a text"
        }
    },

    props:{
        msg:{
          type: String,
          default:"sdgfjsdf"
        }
    },

    computed:{
        hello(){
           return `${this.status} and ${this.mymodel}`
        }
    },

    methods:{
        Clickme(){
            this.$emit("add-event")
            if(this.status=="shweta"){
                this.status="swapnesh"
            }else{
                this.status="shweta"
            }

            console.log(this.$refs["mohit"])
        }
    },

    newtext(e){
        this.mymodel = e.target.value
    }
}

</script>

<style>

</style>

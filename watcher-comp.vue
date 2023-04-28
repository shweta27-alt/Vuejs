<template>
    <div>
        <h1>{{ count }}</h1>
        <button v-on:click="count=count+1"> + </button>
        <button v-on:click="count=count-1"> - </button>
    </div>
    
</template>

<script>


export default{
    data(){
        return{
            count:0
        }
    },

    watch:{
        count(){
            alert("data changes")
        }
    }
}

</script>

<style >

</style>

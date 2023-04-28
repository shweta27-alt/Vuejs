<template>
    <div>
      <!-- <h1 v-bind:class="status" ref="mohit">{{status}}</h1>
      <button @click="Clickme">Bin</button>
      <input v-bind:value="newmodel"  @input ="newmeth" type="text"/>
      <div v-show="learn">Sanjana </div> -->

    <!-- <div >{{hello}}</div> -->

   
    </div>
</template>

<script>
export default{
//    name:'Login',
    
    data(){
      return {
      status:"shweta",
      newmodel:"mohit",
      learn:false
      }
    },
    props:{
      msg:{
        type: String,
        // default:"jahfdsjbhz"
        
      }
    },
   
    computed:{
      hello(){
        return `${this.status}  and ${this.newmodel} `
      }
   
    },

    methods:{
     Clickme(){
      this.$emit("some-event")
      console.log(this.$refs["mohit"].focus())
      if(this.status=="shweta"){
        this.status="swapnesh"
      }else{
        this.status="shweta"
      }
     },
     newmeth(e){
      this.newmodel=e.target.value;
     }
    },
     beforeCreate(){
      console.log("beforecreat")
     },
     created(){
      console.log("created")
     },
     beforeMount(){
      console.log("beforemount")
     },
     mounted(){
      console.log("mounted")
     },
     beforeUpdate(){
      console.log("beforeUpdate")
     },
     updated(){
      console.log(this.newmodel)
      console.log("updated")
     },
      beforeUnmount(){
      console.log("beforeDestroy")
     },
     unmounted(){
      console.log("destroyed")
     }

}

</script>

<style>
 .text{
    color: blueviolet;
    font-size: 25px;
    background-color: aqua;
    height:50px;
    width:200px;
 }

</style>

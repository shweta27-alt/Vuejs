<template>
    <div class="container">
  <h1 v-bind:value="somevalue">
    {{ somevalue }}

    {{ msg }}
  </h1>

  <button v-on:click="Clickme"> Clickme</button>
  <br>

  <input v-model="what" type="text"/>

  <br>

  <input v-bind:value="what" @input="newmeth" type="text"/>

  <br>

  <h1 v-if="modeldata"> {{ modeldata? "shweta" : "mohit" }}</h1>
   

  <div v-show="vuedata">{{ vuedata? "wow" : "yakkk" }}</div>
 

    </div>

</template>

<script>
export default {
    name: "revision-alltags",
    props:{
      msg: String
    },
    data(){
        return{
            somevalue:"hey shweta",
            what:"write something",
            modeldata:"value",
            vuedata:"jhd"
        }
    },


    methods:{
      Clickme(){
        this.$emit("some-value")
        if(this.somevalue=="hey shweta"){
            this.somevalue="you are brave!"
        }else{
            this.somevalue="hey shweta"
        }
      }
    },
   
    newmeth(e){
        this.what=e.target.value;
    }
}
</script>

<style>
.container{
    height: 500px;
    width:500px;
    position:absolute;
    top:50%;
    left:50%;
    transform: translate(-50%,-50%);
}

</style>
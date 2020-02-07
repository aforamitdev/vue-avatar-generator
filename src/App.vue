<template>
<div class="bg-gray-300 min-h-screen text-center py-10">
  <div class="text-xl text-semibold p-6 text-gray-800">Enter Your favourite string</div>
  <input type="text" class="border rounded-lg px-3 py-3 bg-gray-600 text-gray-100 focus:bg-gray-200 focus:text-gray-800" placeholder="Enter string" v-model="input" v-on="onInput()">
  
  <div class=" flex items-center justify-center py-10" v-html="identicon"></div>
  <div class="container mx-auto border border-blue-900 bg-gray-400 p-4">
    {{identicon}}
  </div>
</div>
</template>

<script>

import jdenticon from "jdenticon";
export default {
  name: 'app',
  components: {
  },
  data:()=>{
    return {
      input:""
    }
    
  },
  methods:{
    onInput:function(){
      console.log(this.input)
    }
  },
  computed:{
    identicon:function(){
      return jdenticon.toSvg(this.input,200)
    }
  }
}
</script>

<style>

</style>

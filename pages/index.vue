<template>
 
 <div class="h-screen">
  <div class="w-[80%] rounded-lg p-[2%] bg-amber-100 border-2">
    <p class="flex justify-center items-center font-semibold text-6xl">PokeDex</p>
  </div>
  <!-- <cardpokemon v-for="i in 10" :key="i"/> -->
  <div class="grid grid-cols-3 w-[100%]">
    <cardpokemon v-for="i in response" :key="i" :nombre="i.name" :url="i.url"/>
  </div>

 
 
 </div>


</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return{
      response:[ ]
    }
  },
  mounted(){
    this.getInfo()
  },
  methods:{
     async getInfo(){
      const {data}= await this.$axios.get('pokemon')
      this.response=data.results
      console.log(data)
    }
  }

}
</script>

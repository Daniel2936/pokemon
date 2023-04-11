<template>
    <div class="w-[20%] bg-red-200">
        <!-- <img src="/logo coex.jpg" alt=""> -->
        <img :src="url" alt="">
        <p class="text-center text-2xl font-bold">{{ nombre }}</p>
    </div>
</template>
    
<script>

export default {
    name: 'Cardcomponent',
    props:{
        nombre:{
            type:String,
            requiered:true
        },
        url:{
            type:String,
            requiered:true
        }
    }

  }
    
</script>
    

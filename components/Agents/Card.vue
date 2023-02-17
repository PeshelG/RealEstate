<template>
    <div>
       <div @click="push(agents.id)" class="flex flex-col border border-gray-200 rounded-2xl hover:shadow-lg duration-300 max-md:flex-row max-md:h-fit">
      <div class="object-cover hover:opacity-90 duration-300 max-md:w-1/2">
          <img src="@/assets/images/house2.webp" class="rounded-t-lg h-64 object-cover max-md:h-full max-md:rounded-none max-md:rounded-l-md" alt="">
      </div>
      <div class="p-2 max-md:h-fit max-md:p-1">
          <p class="text-gray-300 text-sm">Agent</p>
          <div class="flex flex-row justify-between text-lg font-medium"><p>Name: {{agents.firstname}} {{agents.lastname}}</p><label class="text-[var(--sendaryyellow)]">{{ agents.rating }}</label></div>
          <p class="text-[var(--secondary)] font-semibold text-lg">Email: {{ agents.email }}</p>
          <p class="text-[var(--secondary)] font-semibold text-lg">Mobile: {{ agents.mobile }}</p>
          <p class="text-red-300 text-sm mt-2">Host: ProperyMeme</p>
      </div>
    </div>
    </div>
   
  </template>
  
  <script>
  export default {
    props: {
      agents: {
        type: Array,
        required: false,
      },
    },
    methods:{
      push(id){
        this.$router.push("/agents/" + this.agents.id)
      }
    }
  }
  </script>
  
  <style>
  .tags{
      font-size: 12px;
  }
  </style>
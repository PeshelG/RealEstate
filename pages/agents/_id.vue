<template>
  <div>
    <div class="wall h-64 bg-gray-500">
        <div class="layout text-white flex flex-row justify-between p-10">
             <div>
             <h1 class="text-3xl font-semibold">Agent Name: </h1>
        <p>Get best deals</p>
        </div>
       <div class="flex flex-row gap-2">
        <p>Share</p>
        <p class="text-red-500">Report</p>
        <p class="text-yellow-400">Overall Rating: 4.3</p>
       </div>
        </div>
       <img src="@/static/logo.png" class="layout bg-white border-2 border-[var(--primary)] w-32 h-32 rounded-full p-20 m-5 object-contain"  alt="">
       <Detail class="layout"/>
    </div>
    <div>

    </div>
  </div>
</template>

<script>
import Detail from '../../components/Agents/Detail.vue';

export default {
    components: { Detail }
}
</script>

<style scoped>
.wall{
    background-image: url('@/assets/images/wallpaper.webp');
    background-size:cover;
    background-repeat: no-repeat;
}
.layout{
    margin: 0px 200px;
}
</style>
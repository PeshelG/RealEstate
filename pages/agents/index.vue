<template>
  <div>
    <h1 class="m-5 text-center">Agent List</h1>
    <div class="grid grid-cols-1 gap-4 py-5 px-5 md:grid-cols-3 md:px-10 xl:grid-cols-4 lg-20">
        <Card v-for="(agent,index) in agents" :key="index" :agents="agent"/>
    </div>
    
    
  </div>
</template>

<script>
import Card from '../../components/Agents/Card.vue';

export default {
    data() {
        return {
            agents: [
                {
                    "id": 4,
                    "firstname": "Munashe",
                    "lastname": "Nzira",
                    "email": "nziramue@gmail.com",
                    "password": "1234",
                    "mobile": "0717201539",
                    "roles": "OWNER",
                    "rating": "string"
                },
                {
                    "id": 5,
                    "firstname": "Precious",
                    "lastname": "Nzira",
                    "email": "nzirape@gmail.com",
                    "password": "1234",
                    "mobile": "0712351539",
                    "roles": "OWNER",
                    "rating": "string"
                }
            ]
        };
    },
    components: { Card }
}
</script>

<style>

</style>
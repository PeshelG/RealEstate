<template>
    <div class="layout md:px-20">
        <p></p>
        <Detail :property="property"/>
    </div>
    
  </template>
  
  <script>
    import Detail from '~/components/Home/Detail.vue';
  export default {
  components:{
Detail
  },
  data(){
    return{
        property: [
  {
    "id": 1,
    "area": "1000SQRT",
    "bedrooms": 7,
    "bathrooms": 2,
    "description": "Lovely Place",
    "features": "string",
    "price": 350,
    "active": false,
    "latitude": 0,
    "longitude": 0,
    "propertyType": "INDUSTRIAL",
    "propertyCondition": "IMMACULATE",
    "subscriptionExpiryDate": "2023-02-16T13:15:02",
    "location": {
      "id": 3,
      "name": "DZIVARASEKWA",
      "density": "HIGH"
    },
    "propertyOwner": null,
    "titleDeed": null
  },
  ],
  id:null,
    }
  },
  mounted(){
    this.id = this.$route.params.id;
    alert("House id: " + this.id)
  }
  }
  </script>
  
  <style>
 
  </style>
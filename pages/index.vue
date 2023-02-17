<template>
  <div class="div">
     <FIlters/>
     <div>
    <div class="grid grid-cols-1 gap-4 py-5 px-5 md:grid-cols-3 md:px-10 xl:grid-cols-4 lg-20">
    <ProductCard v-for="(house,index) in properties" :key="index" :properties="house"/>
  </div>
  <button class="floating bg-gray-800 text-gray-300 py-2 px-4 text-sm rounded-2xl shadow-lg">Open Map</button>

  </div>
  </div>
 
</template>

<script>
import FIlters from '../components/filters/FIlters.vue';
// import ProductList from '../components/Home/ProductList.vue';
import ProductCard from '../components/Home/ProductCard.vue';

export default {
    name: "IndexPage",
    components: { FIlters,ProductCard },
    data(){
      return{
        properties: [
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
  {
    "id": 2,
    "area": "4000SQRT",
    "bedrooms": 11,
    "bathrooms": 4,
    "description": "Great Place",
    "features": "swimming pool",
    "price": 550,
    "active": false,
    "latitude": 0,
    "longitude": 0,
    "propertyType": "COTTAGES_GARDEN_FLATS",
    "propertyCondition": "IMMACULATE",
    "subscriptionExpiryDate": "2023-02-16T13:15:02",
    "location": {
      "id": 7,
      "name": "BELVEDERE",
      "density": "AVONDALE"
    },
    "propertyOwner": null,
    "titleDeed": null
  },
  {
    "id": 3,
    "area": "4000SQRT",
    "bedrooms": 12,
    "bathrooms": 4,
    "description": "Awesome",
    "features": "swimming pool",
    "price": 1250,
    "active": false,
    "latitude": 0,
    "longitude": 0,
    "propertyType": "HOUSES",
    "propertyCondition": "IMMACULATE",
    "subscriptionExpiryDate": "2023-02-16T13:15:02",
    "location": {
      "id": 9,
      "name": "GLENARA",
      "density": "MEDIUM"
    },
    "propertyOwner": {
      "id": 4,
      "firstname": "Munashe",
      "lastname": "Nzira",
      "email": "nziramue@gmail.com",
      "password": "1234",
      "mobile": "0717201539",
      "roles": "OWNER",
      "rating": "string"
    },
    "titleDeed": null
  },
  {
    "id": 4,
    "area": "4500SQRT",
    "bedrooms": 12,
    "bathrooms": 4,
    "description": "Awesome place, very big area",
    "features": "swimming pool",
    "price": 1750,
    "active": false,
    "latitude": 0,
    "longitude": 0,
    "propertyType": "HOUSES",
    "propertyCondition": "IMMACULATE",
    "subscriptionExpiryDate": "2023-02-16T13:15:02",
    "location": {
      "id": 11,
      "name": "BORROWDALE BROOKE",
      "density": "LOW"
    },
    "propertyOwner": null,
    "titleDeed": null
  }
]
      }
    }
}
</script>

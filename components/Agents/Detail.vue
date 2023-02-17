<template>
    <div class="max-md:p-5">
      <h1 class="text-4xl font-bold max-md:text-2xl">Harare</h1>
      <div class="text-gray-400 flex flex-row justify-between mb-5">
          <div>
          <label>Hosted by: PropertyMe</label>
          <label>4.5</label>
          <label>Reviews</label>
          </div>
         <div class="flex flex-row">
          <p class="m-2">Share</p>
          <p class="m-2">Like</p>
         </div>
      </div>
      <div class="flex flex-row mt-10">
          <!-- Contact Info -->
          <div class="contactinfo w-2/3 max-md:mx-5 max-md:w-full">
  <div class="flex flex-row justify-between">
      <div class="flex flex-col">
              <h1 class="text-2xl font-bold">No 122 Emarald Hill, Harare</h1>
              <p class="text-sm bg-red-200 text-red-400 p-1 px-3 rounded-lg w-fit">5 Rooms . Wifi . Borewater</p>
      </div>
      <img src="@/static/logo.png" alt="" class="rounded-4xl w-20 h-20 object-contain" srcset="">
  </div>
  <div class="border-t border-b p-2 py-5">
      <div class="flex flex-row items-center py-2">
      <img src="@/static/logo.png" alt="" class="rounded-4xl w-20 h-20 object-contain" srcset="">
      <div class="flex flex-col">
          <h1 class="text-xl font-bold">Great for remote work</h1>
          <p class="text-md text-gray-400">Fast wifi at 540 Mbps, plus a dedicated workspace in a common area.</p>
      </div>
      </div>
      <div class="flex flex-row items-center py-2">
      <img src="@/static/logo.png" alt="" class="rounded-4xl w-20 h-20 object-contain" srcset="">
      <div class="flex flex-col">
          <h1 class="text-xl font-bold">Great for remote work</h1>
          <p class="text-md text-gray-400">Fast wifi at 540 Mbps, plus a dedicated workspace in a common area.</p>
      </div>
      </div>
      <div class="flex flex-row items-center py-2">
      <img src="@/static/logo.png" alt="" class="rounded-4xl w-20 h-20 object-contain" srcset="">
      <div class="flex flex-col">
          <h1 class="text-xl font-bold">Great for remote work</h1>
          <p class="text-md text-gray-400">Fast wifi at 540 Mbps, plus a dedicated workspace in a common area.</p>
      </div>
      </div>
  
  </div>
  <div class="mt-5">
      <h1 class="text-black text-xl">About Host</h1>
      <p class="text-sm text-gray-400 text-justify">Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium corrupti eaque error maxime, nulla nostrum similique voluptates neque, impedit facere asperiores magnam itaque laborum veritatis nemo aliquam? Repellendus, ut adipisci? Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aperiam et soluta ab veniam aliquam, quod accusantium repellat voluptates fugiat at consequatur dolore animi odit adipisci blanditiis quae nulla beatae voluptatem?</p>
  </div>
  <div class="mt-5">
      <h1 class="text-black text-xl">What this place offers</h1>
      <ul class="text-sm text-gray-400 grid grid-cols-4 gap-3">
          <li>Wifi</li>
          <li>Wifi</li>
          <li>Wifi</li>
          <li>Wifi</li>
          <li>Wifi</li>
      </ul>
  </div>
  
          </div>
          <!-- Ending Contact Info -->
          <div class="sticky contact w-1/3 mx-5 border rounded-lg text-[var(--secondary)] p-5 flex flex-col shadow-lg h-fit">
        <ContactForm/>
          </div>
      </div>
      <h1 class="my-10 text-2xl text-black font-semibold">Listed Properties</h1>
      <div class="grid grid-cols-1 gap-4 py-5 px-5 md:grid-cols-3 md:px-10 xl:grid-cols-4 lg-20 mt-10">
    <ProductCard v-for="(house,index) in properties" :key="index" :properties="house"/>
  </div>
    </div>
  </template>
  
  <script>
  import ContactForm from '@/components/Home/ContactForm.vue'
import ProductCard from '@/components/Home/ProductCard.vue';


export default {
    name: "IndexPage",
    components: { ContactForm,ProductCard },
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

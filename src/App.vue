<template>
  <div>
  <!-- Step , you must use the component -->
  <MyHeader CompanyTitle="Car Showroom" Manager="NAGA PRAVEEN YADALI" />
   <CarBox :CarDetails=CarDetails />
  </div>
</template>

<script>

// step 1 import the child component
import MyHeader from './components/MyHeader.vue'
import CarBox from './components/CarBox.vue'

// 

export default{
 name: 'App',
 // step 2: register the component 
 components:{
   MyHeader,
   CarBox
 },
 data(){
   return {
    CarDetails: []
   }
 },
 methods:{
   //promises
   async fetchCarDetails(){
     const res = await fetch(" http://localhost:3034/api");
     const data = await res.json()
     console.log(data)
     return data
   }
 },
 async created(){
   this.CarDetails = await this.fetchCarDetails();

 }
 

}


</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
  background-color: #488286;
}


div {
  margin-bottom: 0.5em;

}

</style>
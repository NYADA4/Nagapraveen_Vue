<template>
  <div :class="car.instock ? 'green' :'red' ">
      <h2>Model   : {{car.model}}</h2>
      <h2>Price   : {{car.price}} </h2>
      <h2>Year    : {{car.year}} </h2>
      <h2>Miles   : {{car.miles}} </h2>
      <h2>Instock : {{car.stock}}</h2>
  </div>
</template>
<script>

export default {
  name: 'SingleCar',
    props: {
        car: Object
    }
  
}
</script>

<style scoped>
.green{
background-color: rgb(116, 185, 146);
}
h2{
  font-size: 1em;
}
h4{
margin: 2px
}
div{
    margin: 10px;
    padding: 10px;
    text-decoration: none;
    border-radius: 10px;
    display: inline-grid;
    width: 80%;
    height: 200px;
    border: 2px solid #F7F9F9;
}

.red{
background-color: rgb(243, 96, 59) ;
}

</style>
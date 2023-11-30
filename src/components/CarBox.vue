<template>
    <div>
        
        <div v-for="(car, index) in CarDetails.CarDetails" :key="index">
            <SingleCar :car="car" />
        </div>

    </div>      
</template>
<script>
import SingleCar from './SingleCar.vue'
export default{

    name:'CarBox',
    props:{
        CarDetails: Object
    },
    components:{
        SingleCar
    }
}
</script>
<style scoped>
div{
    text-align: center;
    align-items: center;
}
</style>
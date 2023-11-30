<template>
    <div>
        <h1>welcome to Car Showroom </h1>
        <h2>{{ CompanyTitle }}</h2>
        <h4>{{ Manager }}</h4>
    </div>
</template>
<script>
export default {
    name: "MyHeader",
    props: {
        CompanyTitle: String,
        Manager: String
    }
}
</script>
<style scoped>
div {
    text-align: center;
    
}

</style>
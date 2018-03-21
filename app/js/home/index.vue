<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Money/>
        <Product/>
        <Insurance/>
        <carAndMoney/>
        <Footor/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./hslider.vue"
import Insurance from "./insurance.vue"
import Money from "./money.vue"
import Product from "./product.vue"
import CarAndMoney from "./carAndMoney.vue"

export default {
    components: {
        Heador, Slider, Insurance, Money, Product, CarAndMoney, Footor, Navbar,
    },
}
</script>

<style lang="css">
  body{
    background: #eee;
  }
</style>

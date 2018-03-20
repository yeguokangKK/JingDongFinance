<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Selector/>
        <Navbar/>
    </div>

</template>

<script>
import Heador from "../public/header.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./hslider.vue"
import Selector from "./moneySelect.vue"
export default {
    components: {
        Heador, Navbar, Slider, Selector,
    },
}
</script>

<style lang="css">
  body{
    background: #eee;
  }
</style>

<template lang="html">
  <section :class="cname">
    <swiper :options="options" :not-next-tick="options.notNextTick">
      <swiper-slide v-for="item in items" :key="item.href">
        <router-link :to="{ name: item.href}">
          <img :src="item.src" alt="">
        </router-link>
      </swiper-slide>
      <div class="swiper-pagination" v-if="options.pagination"/>
    </swiper>
  </section>
</template>

<script>
import {swiper,swiperSlide} from 'vue-awesome-swiper'
export default {
  components:{
    swiper,
    swiperSlide
  },
  props:{
    options:{
      type:Object,
      default(){
        return{
          autoplay:true,
          loop:true,
          pagination:{
            el:'.swiper-pagination',
          },
          notNextTick:false,
        }
      }
    },
    items:{
      type:Array,
      default(){
        //格式{href:'',src:''},跳转的链接和图片的地址
        return []
      }
    }
  }
}
</script>

<style lang="css">
  @import "~swiper/dist/css/swiper.css"
</style>

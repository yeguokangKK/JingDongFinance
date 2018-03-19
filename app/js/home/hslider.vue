<template lang="html">
    <article class="">
        <Slider :item="items" :cname="$style.slider"/>
        <section class="$style.list">
            <div class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{ name: item.href }">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{ item.title }}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
import Slider from "../core/slider.vue"
export default {
    components: {
        Slider,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t19705/143/810793588/48570/8d28221a/5aab9d90N586fdb3e.jpg?width=750&height=320",
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t18889/265/836165923/44220/e90023b7/5aab9dc2N6b5c9b99.jpg?width=750&height=320",
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t15889/87/2384955814/33715/50b5a382/5aab9de5N82a504c5.jpg?width=750&height=320",
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t15754/56/2447393459/32827/e785366c/5aab9e09Nfb112b5e.jpg?width=750&height=320",
            }],
            enters: [
                {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                    title: "优惠券",
                }, {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                    title: "领红包",
                },
                {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
                    title: "抢钢镚",
                },
                {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                    title: "白条提额",
                },
            ],
        }
    },
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss"
  .slider{
    margin-top:120px;
  }
  .list{
    @include list(row);
    background: #fff;
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around;
    a{
      text-decoration: none;
    }
    .item{
      text-align: center;
      img{
        display: inline-block;
        width: 90px;
        height: 90px;
      }
      h4{
        font-size: 26px;
        margin-top: 12px;
        color: #666;
      }
    }
  }
</style>

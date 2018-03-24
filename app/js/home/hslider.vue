<template lang="html">
    <article>
        <Slider :items="items" :cname="$style.slider"/>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <img :src="item.img" :alt="item.title">
                <h4>{{ item.title }}</h4>
            </div>
        </section>
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t16531/88/2488276313/43844/23edbd44/5ab0c74dN7b559f4f.jpg?width=750&height=220" alt="">
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
                src: "//img12.360buyimg.com/jrpmobile/jfs/t18847/279/921894012/50858/f5a64f65/5ab0e217Nb4ba0199.jpg?width=750&height=320",
            },
            {
                href: "money",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t15043/22/2700496190/48815/dc123010/5ab0e324Nebb21e1c.jpg?width=750&height=320",
            },
            {
                href: "ious",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t19306/294/921741081/36893/92d382f1/5ab0e355N85137f3a.jpg?width=750&height=320",
            }],
            enters: [
                {
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                    title: "优惠券",
                },
                {
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                    title: "领红包",
                },
                {
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
                    title: "抢钢镚",
                },
                {
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                    title: "白条提额",
                },
            ],
        }
    },
}
</script>


<style lang="scss" module>
  @import "../../css/element.scss";
  .slider{
    margin-top:80px;
    img{
      width:100%;
    }
  }
  .list{
    @include list(row);
    background: #fff;
    padding-top: 10px;
    padding-bottom: 20px;
    justify-content: space-around;
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
  article{
    img{
      width:100%;
      display: block;
      margin-top: 20px;
      max-height: 270px;
    }
  }

</style>

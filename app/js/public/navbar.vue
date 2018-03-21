<template lang="html">
    <Panel title="导航条" :class="$style.panel">
        <section :class="$style.content">
            <ul :class="$style.item" v-for="item in items" :key="item.text">
                <li>
                    <router-link :to="{ name: item.href}">
                        <img :src="item.src" alt="">
                        <p>{{ item.text }}</p>
                    </router-link>
                </li>
            </ul>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3451/188/644771475/2428/800d7cb7/580f2435Nbfaa8055.png?width=66&height=66",
                text: "首页",
            },
            {
                href: "money",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3811/55/345433999/2930/116d3dd1/580f1e25N028a1f2c.png?width=66&height=66",
                text: "理财",
            },
            {
                href: "ious",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3343/179/621044750/1484/5af6b11a/580f50e4N005181d0.png?width=66&height=66",
                text: "白条",
            },
            {
                href: "download",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3340/68/639059082/2591/800e2d6b/580f51cdN4caf20b2.png?width=66&height=66",
                text: "我的",
            }],
        }
    },
    created() {
        this.handleChange()
    },
    methods: {
        handleChange() {
            const href = location.href
            const currentPage = href.split("/").pop()
            switch (currentPage) {
                case "": this.items[0].src = "//img12.360buyimg.com/jrpmobile/jfs/t3541/110/627394787/2190/5d02d39c/580f1dfdNcf72af31.png?width=66&height=66"
                    break
                case "money": this.items[1].src = "//img12.360buyimg.com/jrpmobile/jfs/t3559/44/615554467/2520/21aa9352/580f2400N4a7b5398.png?width=66&height=66"
                    break
                case "ious": this.items[2].src = "//img12.360buyimg.com/jrpmobile/jfs/t3673/27/676974575/1305/3f51b3c1/580f4e6eN6efa3e03.png?width=66&height=66"
                    break
                default: this.items[0].src = "//img12.360buyimg.com/jrpmobile/jfs/t3541/110/627394787/2190/5d02d39c/580f1dfdNcf72af31.png?width=66&height=66"
            }
        },
    },
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    position: fixed;
    left: 0;
    right:0;
    bottom:0;
    height: 100px;
    margin:0;
    z-index: 100;
    >h4{
      display: none;
    }
    .content{
      @include flex(row);
      justify-content: space-around;
      .item{
        width: 25%;
      }
      li{
        text-align: center;
        a{
          text-decoration: none;
        }
        img{
          width: 44px;
          height:44px;
          display: inline-block;
          margin:12px auto 6px;
        }
        p{
          font-size: 22px;
          color:#656565;
        }
      }
    }
  }
</style>

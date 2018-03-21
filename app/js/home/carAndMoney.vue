<template lang="html">
    <Panel title="有车有钱" :class="$style.panel">
        <div :class="$style.car">
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t17800/224/698056253/28974/d3ad0665/5aa0ec80N348451f8.png?width=375&height=233" alt="">
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t14215/140/1757206721/24186/81b4e53c/5a56c877Nee6cfc4d.jpg?width=375&height=233" alt="">
        </div>
        <ul :class="$style.content">
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t12799/50/704102454/5247/19eac80a/5a4f2622Nc4aca701.png?width=90&height=90" alt="">
                <p>旅游</p>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t16033/196/1306232362/4705/4c678227/5a4f265bN66ef5ae8.png?width=90&height=90" alt="">
                <p>医美</p>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t13051/63/2559290659/4702/e4068917/5a4f2693N937f1905.png?width=88&height=88" alt="">
                <p>房抵贷</p>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t15133/16/1440686097/5786/1b038e03/5a4f26bfN03ed1f66.png?width=90&height=90" alt="">
                <p>驾校</p>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t14896/125/1435676873/3668/a8b392f7/5a4f26edN6cdfda66.png?width=88&height=88" alt="">
                <p>分期用</p>
            </li>
        </ul>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    .car{
      box-sizing: border-box;
      img{
        width:45%;
        max-height: 233px;
        display: inline-block;
        padding-left: 18px;
      }
    }
    .content{
      @include flex(row);
      box-sizing: border-box;
      padding-bottom: 40px;
      .item{
        width:20%;
        text-align: center;
        img{
          width:88px;
          height: 88px;
        }
        p{
          font-size:26px;
          color:#666;
          text-overflow: ellipsis;
          white-space: nowrap;
          overflow: hidden;
          margin-top: 12px;

        }
      }
    }
  }
</style>

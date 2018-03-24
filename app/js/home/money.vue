<template lang="html">
    <Panel title="理财精选" :class="$style.panel">
        <section :class="$style.content">
            <dl :class="$style.item" v-for="item in items" :key="item.title">
                <dt>{{ item.title }} <span :class="$style.red">{{ item.sub }}</span></dt>
                <dd>{{ item.rate }}</dd>
                <dd>{{ item.text }}</dd>
            </dl>
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
                title: "定期理财",
                sub: "90天可质押",
                rate: "5.50%",
                text: "历史年化结算利率",
            },
            {
                title: "固收理财",
                sub: "理财推荐",
                rate: "5.80%",
                text: "综合年化收益率",
            },
            {
                title: "基智账户",
                sub: "组合投资",
                rate: "8%~10%",
                text: "止盈年化收益率",
            },
            {
                title: "小白基金",
                sub: "超短期",
                rate: "5.00%",
                text: "7日年化收益率",
            }],
        }
    },
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel{
  @include panel;
  .content{
    @include flex(row);
    justify-content: space-around;
    box-sizing: border-box;
    &:after{
      content:" ";
      display: block;
      width: 100%;
      height: 0px;
      box-sizing: border-box;
      border-bottom: 1px solid #4d4d4d;
      /*把贯穿的横线移到中间*/
      position: relative;
      top:-208px;
    }
    .item{
      position: relative;
      width: 50%;
      box-sizing: border-box;
      /*添加竖线*/
      &:after{
        content: " ";
        width:1px;
        height: 136px;
        display: block;
        position: absolute;
        top:50%;
        right:0;
        margin-top: -68px;
        border-right: 1px solid #4d4d4d;
      }
      &:nth-child(2n){
        &:after{
          display: none;
        }
      }
      padding:34px 16px;
      dt{
        font-size: 30px;
        line-height: 42px;
        color:#333;
        span{
          font-size: 22px;
          color:#ff5155;
          border:1px solid #ff5155;
          padding:0 8px;
          /*调整文字对齐*/
          vertical-align: 1px;
          margin-left: 2px;
        }
      }
      dd{
        &:nth-child(2){
          font-weight: 700;
          font-size: 44px;
          height: 58px;
          line-height: 58px;
          color:#FF5155;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        }
        &:nth-child(3){
          font-size: 24px;
          height: 34px;
          line-height: 34px;
          color:#999;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        }
      }
    }
  }
}

</style>

<template lang="html">
    <div :class="[btnClass,cname]">
        <slot/>
    </div>
</template>

<script type="text/javascript">
export default{
    props: {
        cname: {
            type: String,
            default: "",
        },
    },
    data() {
        return {
            btnClass: "btn",
        }
    },
}
</script>

<style lang="scss">
@import "../../css/element.scss"
.btn{
  @include btn;
}
</style>

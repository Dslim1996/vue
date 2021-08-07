<template>  <!--최상위 요소(루트) : 2개 이상 있는경우 class rim 이 어디 들어갈지 모름 -->
    <div class="btn"> <!--class = rim 상속 -->
        <slot></slot> <!--{{ text }} -->
    </div>
    <!--<h1 :class="$attrs.class" :style="$attrs.style"></h1>-->
    <h1 v-bind="$attrs"></h1>
</template>

<script>
export default {
    inheritAttrs: false,
    created() {
        console.log(this.$attrs)
    }
}
</script>


<style lang="scss" scoped>
    .btn {
        display: inline-block;
        margin: 4px;
        padding: 6px 12px;
        border-radius: 4px;
        background-color: gray;
        color:white;
        cursor: pointer;
    }
</style>

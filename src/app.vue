<template>
    <MyBtn>Banana</MyBtn>
    <MyBtn color="#000">Apple</MyBtn>
    <MyBtn :col="color">
        <span style="color: red">bababa</span>
    </MyBtn>
    <MyBtn large col="royalblue" text="Banana" />

    <button>banana</button>
</template>

<script>
import MyBtn from "~/components/MyBtn";   

export default {
    components: {
        MyBtn
    },
    data() {
        return {
            color: 'black'
        }
    }
}
</script>


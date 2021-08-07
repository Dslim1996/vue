<template>
    <MyBtn 
    @rim="log" 
    @change-msg="logMsg">
        Banana
    </MyBtn>
</template>

<script>
import MyBtn from "~/components/MyBtn";   

export default {
    components: {
        MyBtn
    },
    methods: {
        log(e) {
            console.log('Click!!')
            console.log(e)
        },
        logMsg(msg){
            console.log(msg)
        }
    }
}
</script>


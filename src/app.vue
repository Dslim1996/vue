<template>
    <button @click="handlerA(), handlerB()">
        click me
    </button>
</template>

<script>

export default {
    methods: {
        handlerA(){
            console.log('A')
        },
        handlerB(){
            console.log('B')
        }
    }
}
</script>

<template>
    <a 
    href="https://naver.com"
    target="_blank"
    @click.prevent.once="handler">
    NAVER
    </a>

    <div 
    class="parent"
    @wheel.passive="handlerC">
        <div 
        class="child"></div>
    </div>

    <input 
    type="text" 
    @keydown.ctrl.shift.a="handler"/>
</template>

<script>

export default {
    methods: {
        handler(){
            console.log('Enter!!')
            
        },
        handlerA(event){
            console.log(event.target)
            console.log(event.currentTarget)
            console.log('A')
        },
        handlerB(){
            console.log('B')
        },
        handlerC(event){
            for(let i = 0; i < 10000; i++){
                console.log(event)
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    .parent{
        width: 200px;
        height: 100px;
        background-color: royalblue;
        margin: 10px;
        padding: 10px;
        overflow: auto;
        .child{
            width: 100px;
            height: 2000px;
            background-color: orange;
        }
    }
</style>
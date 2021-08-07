<template>
    <h1>{{ msg }}</h1>

    <input 
    type="text" 
    v-model.trim="msg"/>
    
    <input 
    type="text" 
    :value="msg" 
    @change="msg = $event.target.value"/>
    
    <input 
    type="text" 
    v-model.lazy="msg"/>
    
    <input 
    type="text" 
    v-model.number="msg"/>
</template>

<script>

export default {
    data() {
        return {
            msg: 'hello world'
        }
    },
    watch: {
        msg() {
            //trim() 앞뒤 공백 제거
            console.log(this.msg)
        }
    }
}
</script>


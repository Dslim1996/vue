<template>
    <h1>한글 입력시 한박자 늦음{{ msg }}</h1>
    <input 
    type="text" 
    v-model="msg" />
    
    <h1>한글 입력시 즉시 입력{{ msg }}</h1>
    <input 
    type="text" 
    :value="msg"
    @input="msg = $event.target.value" />

    <h1>{{ checked }} </h1>

    <input 
    type="checkbox" 
    v-model="checked">
</template>

<script>

export default {
    data() {
        return {
            msg: 'hello world',
            checked: false
        }
    }
}
</script>


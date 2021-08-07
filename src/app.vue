<template>
    <h1 
    v-once
    @click="add">
        {{ msg1 }}
    </h1>

    <h1 
    @click="add">
        {{ msg }}
    </h1>

    <h1 v-html="msg1"></h1>

    <h1 v-bind:class="msg2">
        {{ msg2 }}
    </h1>
    
    <h1 
        :[attr]="'active'"
        @[event]="add">
        {{ msg2 }}
    </h1>

</template>

<script>

export default {
    data() {
        return{
            msg: 'hello',
            msg1: '<div style="color: red;">Hello!!</div>',
            msg2: 'active',
            attr: 'class',
            event: 'click'
        }        
    },
    methods: {
        add() {
            this.msg += "!"
        }
    }
}
</script>

<style scoped>
    .active {
        color: royalblue;
        font-size: 100px;
    }
</style>

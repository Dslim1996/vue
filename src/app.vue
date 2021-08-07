<template>
    <button @click="handler">
       Click me!
    </button>
    <template v-if="isShow">
        <h1>Title</h1>
        <p>Pargraph1</p>
        <p>Pargraph2</p>
    </template>

    <h1 v-show="isShow">
        Hello?!
    </h1>
</template>

<script>
export default {
    data() {
        return {
            isShow: false,
            count: 0
        }
    },
    methods: {
        handler() {
            this.isShow = !this.isShow
            this.count += 1
        }
    }
}   
</script>

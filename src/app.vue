<template>
    <h1 @click="increase">
        {{ count }} / {{ doublecount }}
    </h1>
    <h1 @click="changeMessage">
        {{ message }} / {{ reversedMessage }}
    </h1>
</template>

<script>
export default {
    data() {
        return {
            count: 0,
            message: 'Hello World!'
        }
    },
    computed: {
        doubleCount() {
            return this.count * 2
        },
        reversedMessage() {
            return this.message.split('').reverse().join('')
        }
    },
    watch: {
        message(msg) {
            console.lot(msg)
        }
    },
    created() {
        console.log(this.message)
    },
    mounted() {
        console.lot(this.count)
    },
    methods: {
        increase() {
            this.count += 1
        },
        changeMessage() {
            this.message = 'Good?'
        }
    }
}
</script>

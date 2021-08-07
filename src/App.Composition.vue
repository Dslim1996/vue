<template>
    <h1 @click="increase">
        {{ count }} / {{ doublecount }}
    </h1>
    <h1 @click="changeMessage">
        {{ message }} / {{ reversedMessage }}
    </h1>
</template>

<script>
import { ref, computed, watch, onMounted } from 'vue'

export default {
    set() {
        //create() 작성과 동일한 효과
        const count = ref(0)
        const doubleCount = computed(() => {
            return count.value * 2
        })
        function increase() {
            count.value += 1
        }

        const message = ref('Hello World!')
        const reversedMessage = computed(() => {
            return message.value.split('').reverse().join('')
        })
        watch(message, msg => console.log(msg))
        function changeMessage() {
            message.value = 'Good!'
        }
        console.log(message.value)  //created() 와 도일한 효과

        onMounted(() => {
            console.log(count.value)
        })



        return {
            //count: count,
            //message:message
            count,
            doubleCount,
            increase,
            message,
            reversedMessage,
            changeMessage,
        }
    }
}
</script>
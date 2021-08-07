<template>
    <div @click="increase">
        {{ count }}
    </div>
</template>

<script>
import { ref } from 'vue'

export default {
    setup() {
        //let count = 0 //반응성X
        let count = ref(0) //반응성을 가진 객체 데이터

        function increase() {
            count.value += 1
        }

        return {
            count,
            increase
        }
    }
}
</script>


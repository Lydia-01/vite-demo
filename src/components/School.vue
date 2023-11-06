<script setup>
import { ref } from 'vue'
const name = ref('')
const address = ref('')
const now = ref(new Date())


const timer = setInterval(() => {

    now.value = new Date()

}, 1000)

const StopSet = () => {
    clearInterval(timer)
}

</script>
<template>
    <ul>
        <li>name:{{ name }}</li>
        <li>address:{{ address }}</li>
        <li>{{ now.toISOString() }}</li>
    </ul>
    <button @click="StopSet">停止时间</button>
</template>

<template>
    <div class="container">
        <h1>Nhập tháng của bạn:</h1>
        <input type="number" v-model.number="month"/>
        <P v-if="month < 1 || month >  12" style="color: red;">Vui lòng nhập từ tháng 1-12</P>
        <p v-else-if="month  >= 1 && month <= 3">Mùa xuân</p>
        <p v-else-if="month <= 6">Mùa hạ</p>
        <p v-else-if="month <= 9">Mùa thu</p>
        <p v-else>Mùa đông</p>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const month = ref(1)
</script>
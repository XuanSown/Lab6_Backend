<template>
    <div>
        <h1>Nhập điểm của bạn:</h1>
        <h5>*Lưu ý điểm lớn hơn 0, nhỏ hơn 10</h5>
        <input type="number" v-model="score" min="0"  max="10"/>
        <p v-if="score < 0 || score > 10" style="color: red;">Vui lòng nhập điểm trong khoảng 0-10</p>
        <p v-if="score >= 9">Xuất sắc</p>
        <p v-else-if="score >= 8">Giỏi</p>
        <p v-else-if="score >= 6.5">Khá</p>
        <p v-else>Yếu</p>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const score = ref(0)
</script>
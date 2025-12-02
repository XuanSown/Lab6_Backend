<script setup>
import bai1 from './components/Bai1/bai1.vue';
import bai2 from './components/Bai2/bai2.vue';
import bai3 from './components/Bai3/bai3.vue';
import bai4 from './components/Bai4/bai4.vue';
import { ref } from 'vue';

  const current = ref('bai1');
  const components = { bai1, bai2, bai3, bai4 };
</script>

<template>
<select v-model="current">
    <option value="bai1">Bài 1</option>
    <option value="bai2">Bài 2</option>
    <option value="bai3">Bài 3</option>
    <option value="bai4">Bài 4</option>
</select>
<component :is="components[current]" />
</template>

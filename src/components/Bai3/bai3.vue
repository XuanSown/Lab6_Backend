<template>
    <div class="container-fluid mt-5">
        <h1 class="text-center mb-5 text-primary">Kiến thức sức khỏe cộng đồng</h1>
        <div class="row g-4">
            <div class="col-12 col-md-4" v-for="(item, index) in items" :key="index">
                <div class="card h-100 shadow-sm">
                    <img :src="item.image" class="card-img-top img-fluid rounded"/>
                    <div class="card-body d-flex flex-column">
                        <h3 class="card-title">{{ item.title }}</h3>
                        <p style="text-align: justify;" class="card-text">{{ item.content }}</p>
                        <button class="btn btn-info w-100 mt-auto">Xem chi tiết</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import img1 from '../../assets/images/orange.jpg';
import img2 from '../../assets/images/sesameoil.jpg';
import img3 from '../../assets/images/spinach.jpg';
const items = ([
    { title: '8 loại rau củ quả giàu canxi', content: 'Canxi là khoáng chất cần thiết đối với cơ thể người. Có nhiều cách để bổ sung canxi, trong đó bổ sung qua đường ăn uống là cách tốt nhất. Có 8 loại rau củ giàu canxi...', image: img1 },
    { title: 'Các loại gia vị tốt cho sức khỏe', content: 'Một số loại gia vị cung cấp nhiều polyphenol chống oxy hóa cao hơn các loại gia vị quen thuộc khác. Với một lượng nhỏ các món ăn đã thêm hương thơm và vị hấp dẫn...', image: img2 },
    { title: '9 loại đậu bổ dưỡng nên dùng nhiều', content: 'Đậu lăng, đậu nành, đậu phộng, đậu Hà Lan giàu chất xơ, protein cùng nhiều vitamin và khoáng chất giúp giảm lượng trong máu, tốt cho tim...', image: img3 },
]);
</script>

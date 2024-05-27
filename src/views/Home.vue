<template>
    <div class="q-pa-md">
        <q-carousel
            animated
            v-model="slide"
            navigation
            infinite
            :autoplay="autoplay"
            arrows
            transition-prev="slide-right"
            transition-next="slide-left"
            @mouseenter="autoplay = false"
            @mouseleave="autoplay = true"
        >
            <q-carousel-slide :name="1">
                <img src="../assets/img/bunga1.jpeg" class="carousel-image" alt="Slide 1" />
            </q-carousel-slide>
            <q-carousel-slide :name="2">
                <img src="../assets/img/bunga2.jpg" class="carousel-image" alt="Slide 2" />
            </q-carousel-slide>
            <q-carousel-slide :name="3">
                <img src="../assets/img/bunga3.jpg" class="carousel-image" alt="Slide 3" />
            </q-carousel-slide>
        </q-carousel>
    </div>

    <div class="q-pa-md">
        <q-card class="my-card">
            <q-card-section>
                <div class="text-h6">Selamat datang di ElizzaFlower</div>
                <div class="text-subtitle2">Pesan Bouquet dengan bunga berkualitas di kami!</div>
            </q-card-section>
        </q-card>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
  
    const slide = ref(1);
    const autoplay = ref(true);
</script>

<style scoped>
.my-card {
    max-width: 400px;
    margin: 20px auto;
}

.carousel-image {
    width: 100%; 
    height: 100%; 
    object-fit:cover; 
}
</style>

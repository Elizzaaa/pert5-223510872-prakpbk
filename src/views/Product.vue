<template>
    <div class="q-pa-md card-container">
        <h4 style="text-align:center">Bouquet Kami</h4>
      <div class="grid-container">
        <q-card v-for="product in products" :key="product.id" class="my-card">
          <img :src="product.image" :alt="product.name" size="fit">
            <q-icon name="star" color="white" class="absolute-top-right q-pa-xs" />
          </img>
          <q-card-section>
            <div class="text-h6">{{ product.name }}</div>
            <div class="text-p">{{ product.description }}</div>
            <div class="text-subtitle2">{{ product.price }}</div>
          </q-card-section>
        </q-card>
      </div>
    </div>
</template>
  
<script setup>
  import { ref } from 'vue';
  import bouquetmawar from "../assets/img/bouquetmawar.jpg";
  import bouquettulip from "../assets/img/bouquettulip.jpg";
  import bouquetlily from "../assets/img/bouquetlily.jpg";
  import bouquetorchid from "../assets/img/bouquetorchid.jpg";
  import bouquetlilac from "../assets/img/bouquetlilac.jpg";
  import bouquetdahlia from "../assets/img/bouquetdahlia.jpg";
  
  const products = ref([
    {
      id: 1,
      name: "Bouquet Mawar",
      description: "Bonquet yang dibuat dari bunga mawar",
      price: "Rp45.000",
      image: bouquetmawar,
    },
    {
      id: 2,
      name: "Bouquet Tulip",
      description: "Bonquet yang dibuat dari bunga tulip",
      price: "Rp50.000",
      image: bouquettulip,
    },
    {
      id: 3,
      name: "Bouquet Lily",
      description: "Bonquet yang dibuat dari bunga lily",
      price: "Rp55.000",
      image: bouquetlily,
    },
    {
      id: 4,
      name: "Bouquet Orchid",
      description: "Bonquet yang dibuat dari bunga orchid",
      price: "Rp60.000",
      image: bouquetorchid,
    },
    {
      id: 5,
      name: "Bouquet Lilac",
      description: "Bonquet yang dibuat dari bunga lilac",
      price: "Rp65.000",
      image: bouquetlilac,
    },
    {
      id: 6,
      name: "Bouquet Dahlia",
      description: "Bonquet yang dibuat dari bunga dahlia",
      price: "Rp70.000",
      image: bouquetdahlia,
    },
  ])
</script>
  
<style scoped>
  .grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(25%, 1fr));
    gap: 40px;
  }
  
  .my-card {
    width: 100%;
  }
  
  .card-container {
    margin-top: 20px;
  }
</style>
  
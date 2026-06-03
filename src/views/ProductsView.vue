<script setup lang="ts">

import { ref, onMounted } from "vue";

import api from "../services/api";

import ProductCard from "../components/ProductCard.vue";

interface Product {
  id: string;
  nombre: string;
  precio: number;
  imagen: string;
}

const products = ref<Product[]>([]);

onMounted(async () => {

  try {

    const response = await api.get("/products");

    products.value = response.data.data;

  } catch (error) {

    console.log(error);

  }

});

</script>

<template>

  <div>

    <h1 class="text-4xl font-bold mb-8 text-center">
      Productos
    </h1>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
  <ProductCard
    v-for="product in products"
    :key="product.id"
    :product="product"
  />
</div>

  </div>

</template>
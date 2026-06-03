<script setup lang="ts">

interface Product {
  id: string;
  nombre: string;
  precio: number;
  imagen: string;
}

defineProps<{
  product: Product;
}>();

</script>

<template>

  <div class="card bg-base-100 shadow-xl">

    <figure>
  <img
    :src="product.imagen"
    :alt="product.nombre"
    class="h-48 w-full object-cover"
  />
</figure>

    <div class="card-body">

      <h2 class="card-title">
        {{ product.nombre }}
      </h2>

      <p>
        ${{ product.precio }}
      </p>

    </div>

  </div>

</template>

<script setup lang="ts">

import ProductsView from "./views/ProductsView.vue";
import OrdersView from "./views/OrdersView.vue";

</script>

<template>
  <h1 class="text-6xl font-bold text-center mb-16">
  Ecommerce Dashboard
</h1>


  <div class="min-h-screen bg-base-200 p-10">

    <ProductsView />

    <div class="divider my-10">
      PEDIDOS
    </div>

    <OrdersView />

  </div>

</template>
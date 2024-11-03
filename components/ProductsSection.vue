<template>
    <section id="products" class="py-16 bg-gray-100">
      <div class="container mx-auto px-4 text-center">
        <h2 class="text-4xl font-bold mb-8 text-gray-800">Nuestros Productos</h2>
        <p class="text-lg text-gray-600 mb-12">Explora nuestra colección de productos artesanales de alta calidad hechos con totora.</p>
        
        <!-- Grid de productos -->
        <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
          <ProductCard
            v-for="(product, index) in products"
            :key="index"
            :title="product.title"
            :description="product.description"
            :image="product.image"
          />
        </div>
      </div>
    </section>
  </template>
  
  <script>
  
  export default {
    props: {
      products: {
        type: Array,
        required: true
      }
    }
  };
  </script>
  
  <style scoped>
  /* Puedes agregar estilos adicionales aquí si es necesario */
  </style>
  
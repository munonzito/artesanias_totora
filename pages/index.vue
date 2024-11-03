<template>
    <div>
      <AppNavbar/>
      <div id="inicio" class="relative text-center text-white">
        <img src="public/background/totora_background_1.webp" alt="Hero Image" class="w-full h-screen object-cover">
        <div class="absolute inset-0 flex flex-col items-center justify-center bg-black bg-opacity-50">
          <h1 class="text-5xl md:text-6xl font-extrabold mb-4">
            Descubre la Artesanía en Totora
          </h1>
          <p class="text-lg md:text-2xl max-w-2xl mb-8 px-4">
            Elaboramos productos únicos y sostenibles con materiales de la más alta calidad. Trae un toque de elegancia natural a tu hogar con nuestra colección artesanal.
          </p>
          <div class="flex space-x-4">
            <NuxtLink to="#products" class="bg-orange-600 hover:bg-orange-700 text-white font-semibold py-3 px-6 rounded-lg transition duration-300">
              Ver Productos
            </NuxtLink>
            <NuxtLink to="#contact" class="bg-transparent border border-white hover:bg-white hover:text-black text-white font-semibold py-3 px-6 rounded-lg transition duration-300">
              Contacto
            </NuxtLink>
          </div>
        </div>
      </div>
    
      <ProductsSection id="products" :products="products"/>
      <ContactSection id="contact"/>
      <AboutSection id="about"/>
    </div>
  </template>
  

  <script setup>
 const products = ref([{
          title: "Totora Rústica",
          description: "Descripción breve del producto 1. Perfecto para añadir un toque natural y artesanal a tu hogar.",
          image: "products/product_1.jpeg",
          buttonText: "Ver más"
        },
        {
          title: "Cortinas de Totora",
          description: "Descripción breve del producto 3. Un toque de elegancia artesanal para cualquier ambiente.",
          image: "products/product_3.jpeg",
          buttonText: "Ver más"
        },
        {
          title: "Gorros de Totora",
          description: "Descripción breve del producto 2. Ideal para complementar la decoración de cualquier espacio.",
          image: "products/product_2.jpeg",
          buttonText: "Ver más"
        },
        ])
useHead({
    title: 'Artesanía en Totora',
    meta: [
      {
        name: 'description',
        content: 'Descubre nuestra colección de productos artesanales elaborados con totora. Añade un toque natural y sostenible a tu hogar.'
      }
    ]
  })

</script>
  
<style scoped>
</style>
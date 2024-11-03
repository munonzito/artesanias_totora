<template>
    <section id="contact" class="py-16 bg-gray-100">
      <div class="container mx-auto px-4 flex flex-col lg:flex-row items-center space-x-16">
        
        <!-- Contenido de contacto -->
        <div class="text-center lg:text-left lg:w-1/2 mb-8 lg:mb-0">
          <h2 class="text-4xl font-bold text-gray-800 mb-4">Contáctanos</h2>
          <p class="text-lg text-gray-600 mb-6">
            ¿Tienes alguna pregunta o deseas realizar un pedido? Estamos aquí para ayudarte a adquirir nuestros productos de manera rápida y sencilla. Tu satisfacción es nuestra prioridad y queremos que disfrutes de la mejor experiencia de compra
        </p>
          <!-- Número de teléfono -->
          <p class="text-2xl font-semibold text-gray-700 mb-8">
            📞 +569 6283 2950
          </p>
          
          <!-- Botones de contacto -->
          <div class="flex justify-center lg:justify-start space-x-4">
            <!-- Botón de llamada -->
            <a 
              href="tel:+56962832950" 
              class="bg-orange-600 hover:bg-orange-700 text-white font-semibold py-3 px-6 rounded-lg transition duration-300"
            >
              Llámanos
            </a>
            
            <!-- Botón de WhatsApp -->
            <a 
              href="https://wa.me/56962832950" 
              target="_blank" 
              class="bg-green-600 hover:bg-green-700 text-white font-semibold py-3 px-6 rounded-lg transition duration-300"
            >
              WhatsApp
            </a>
          </div>
        </div>
  
        <!-- Imagen de contacto -->
        <div class="hidden lg:w-1/2 lg:block">
          <img 
            src="public/contact/contact_image.webp" 
            alt="Contacto" 
            class="w-full h-auto rounded-lg shadow-lg"
          />
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "ContactSection"
  };
  </script>
  
  <style scoped>
  /* Puedes agregar estilos adicionales aquí si es necesario */
  </style>
  
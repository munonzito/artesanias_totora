<template>
    <section id="about" class="py-16 bg-white">
      <div class="container mx-auto px-4 flex flex-col lg:flex-row items-center gap-x-16">
        
        <!-- Imagen de la sección -->
        <div class="lg:w-1/2 mb-8 lg:mb-0">
          <img 
            src="public/about/about_image.webp" 
            alt="Equipo de Totora Zuñiga" 
            class="w-full h-auto rounded-lg shadow-lg"
          />
        </div>
        
        <!-- Contenido de la sección "Quiénes Somos" -->
        <div class="text-center lg:text-left lg:w-1/2">
          <h2 class="text-4xl font-bold text-gray-800 mb-4">Sobre Nosotros</h2>
          <p class="text-lg text-gray-600 mb-6">
            En <span class="font-semibold text-orange-600">Totora Zuñiga</span>, nos apasiona la artesanía y la sostenibilidad. Desde nuestros inicios, hemos buscado unir lo tradicional con lo contemporáneo, creando productos únicos que reflejan la esencia de la naturaleza y el trabajo artesanal.
          </p>
          <p class="text-lg text-gray-600 mb-6">
            Cada una de nuestras piezas está hecha a mano con totora, un material natural y renovable que obtenemos de manera responsable. Nos enorgullece brindar a nuestros clientes productos que no solo embellecen sus hogares, sino que también apoyan una economía más ética y respetuosa con el medio ambiente.
          </p>
          <p class="text-lg text-gray-600 mb-6">
            Nuestro equipo está comprometido en cada detalle, asegurando que cada producto de <span class="font-semibold text-orange-600">Totora Zuñiga</span> sea una muestra de nuestra dedicación por la calidad, la creatividad y la naturaleza. ¡Únete a nuestra misión y trae un toque de elegancia artesanal a tu vida!
          </p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "AboutSection"
  };
  </script>
  
  <style scoped>
  /* Puedes agregar estilos adicionales aquí si es necesario */
  </style>
  
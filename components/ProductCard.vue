<template>
    <div class="bg-white rounded-lg shadow-lg p-6 text-start">
      <img :src="image" :alt="title" class="w-full h-64 object-cover rounded-md mb-4">
      <h3 class="text-2xl font-semibold mb-2">{{ title }}</h3>
      <p class="text-gray-600 mb-4">{{ description }}</p>
    <a href="#contact">
      <button class="bg-orange-600 hover:bg-orange-700 text-white font-semibold py-2 px-4 rounded-lg transition duration-300">
        Contáctanos
      </button>
    </a>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
      image: {
        type: String,
        required: true
      },
      buttonText: {
        type: String,
        default: "Ver más"
      }
    }
  };
  </script>
  
  <style scoped>
  /* Puedes agregar estilos adicionales aquí si es necesario */
  </style>
  
<template>
  <nav class="fixed top-0 left-0 w-full bg-white shadow-md z-50">
    <div class="container mx-auto px-4 py-8 flex justify-between items-center">
      <div class="flex items-center">
        <span class="text-xl font-bold text-orange-600">Totora Zuñiga</span>
      </div>
      <button 
        class="text-gray-600 lg:hidden" 
        @click="isMenuOpen = !isMenuOpen"
        aria-label="Toggle navigation"
      >
        <svg v-if="!isMenuOpen" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>

      <ul 
        :class="['lg:flex', isMenuOpen ? 'block' : 'hidden']"
        class="flex flex-col text-center lg:flex-row items-center lg:space-x-8 text-gray-600 font-medium space-y-4 lg:space-y-0 mt-4 lg:mt-0"
      >
        <li>
          <NuxtLink
            class="hover:text-gray-800 hover:underline underline-offset-4"
            :class="{ 'border-b-2 border-orange-600 pb-1': activeSection === 'inicio' }"
            @click.prevent="scrollToSection('inicio')"
          >
            Inicio
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            class="hover:text-gray-800 hover:underline underline-offset-4"
            :class="{ 'border-b-2 border-orange-600 pb-1': activeSection === 'products' }"
            @click.prevent="scrollToSection('products')"
          >
            Nuestros Productos
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            class="hover:text-gray-800 hover:underline underline-offset-4"
            :class="{ 'border-b-2 border-orange-600 pb-1': activeSection === 'contact' }"
            @click.prevent="scrollToSection('contact')"
          >
            Contacto
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            class="hover:text-gray-800 hover:underline underline-offset-4"
            :class="{ 'border-b-2 border-orange-600 pb-1': activeSection === 'about' }"
            @click.prevent="scrollToSection('about')"
          >
            Sobre Nosotros
          </NuxtLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';
import { useRoute } from 'vue-router';

const isMenuOpen = ref(false);
const activeSection = ref('');

const route = useRoute();

// Función para establecer la sección activa
const setActiveSection = (section) => {
  activeSection.value = section;
};

const scrollToSection = (section) => {
  const sectionElement = document.getElementById(section);
  if (sectionElement) {
    // Calcula la posición deseada restando la altura del navbar y 20 píxeles adicionales
    const navbarHeight = 80; // Ajusta esta altura según el tamaño de tu navbar
    const sectionOffset = sectionElement.offsetTop - navbarHeight;
    window.scrollTo({
      top: sectionOffset,
      behavior: 'smooth' // Desplazamiento suave
    });
  }
  setActiveSection(section); // Actualiza la sección activa
};


// Función para actualizar la sección activa según el desplazamiento
const handleScroll = () => {
  const sections = ['inicio', 'products', 'contact', 'about'];
  let scrollPos = window.scrollY;

  sections.forEach(section => {
    const sectionElement = document.getElementById(section);
    if (sectionElement) {
      const sectionOffset = sectionElement.offsetTop;
      const sectionHeight = sectionElement.offsetHeight;

      if (scrollPos >= sectionOffset && scrollPos < sectionOffset + sectionHeight) {
        activeSection.value = section;
      }
    }
  });
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
body {
  padding-top: 80px; /* Ajusta el espacio para el navbar fijo */
}
</style>


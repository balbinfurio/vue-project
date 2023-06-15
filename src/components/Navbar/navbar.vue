


<template>
    <nav class="navbar">
        <div class="navbar-menu">
            <div class="menu-icon" @click="toggleMenu">
                <button>
                    <i :class="['fas', isMenuOpen ? 'fa-times' : 'fa-bars']"></i>
                </button>
            </div>
        <div class="logo">
          <h1>LOGO</h1>
          <!-- Puedes agregar tu propio logo como una imagen o utilizar un componente de imagen -->
        </div>
      </div>

      <transition name="fade">
        <div v-if="isMenuOpen" class="menu-content">
          <!-- Contenido del menú -->
          <ul>
            <li>Elemento 1</li>
            <li>Elemento 2</li>
            <li>Elemento 3</li>
          </ul>
        </div>
      </transition>

      <div class="navbar-search">
        <h1>SEARCH</h1>
        <!-- Puedes utilizar un componente de entrada de texto o personalizarlo según tus necesidades -->
      </div>
      <div class="navbar-config">
        <h1>TUERCA</h1>
        <!-- Puedes utilizar algún icono de configuración de una biblioteca de iconos o un icono personalizado -->
      </div>
      <div class="navbar-icons">
        <i class="fas fa-icon"></i>
        <h1>I1</h1>
        <i class="fas fa-icon"></i>
        <h1>I2</h1>
        <i class="fas fa-icon"></i>
        <h1>I3</h1>
        <!-- Puedes utilizar iconos individuales o agruparlos en un componente -->
      </div>
      <div class="navbar-user">
        <h1>USER</h1>
        <!-- Puedes mostrar el nombre de usuario o personalizarlo según tus necesidades -->
      </div>
    </nav>
  </template>
  
  <script>
  
  import { defineComponent, ref } from 'vue';
  
  export default defineComponent({
    setup() {
      const isMenuOpen = ref(false);
  
      const toggleMenu = () => {
        isMenuOpen.value = !isMenuOpen.value;
      };
  
      return {
        isMenuOpen,
        toggleMenu
      };
    }
  });
  </script>
  
  <style>

  .navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    height: 100px;
    background-color: #1d1f28;
    padding: 0 20px;
    /* Estilos adicionales para el navbar */
  }

  .menu-content {
    background-color: #1d1f28;
    padding: 10px;
    color: #ffffff;
    position: absolute;
    top: 150px;
    left: 0;
    width: 15%;
    z-index: 9999;
    }

    .fade-enter-active,
    .fade-leave-active {
        transition: opacity 0.3s;
    }

    .fade-enter,
    .fade-leave-to {
    opacity: 0;
    }
  
  .navbar-menu {
    display: flex;
    align-items: center;
    /* Estilos adicionales para el menú */
  }
  
  .menu-icon {
    /* Estilos para el icono de menú de 3 rayas */
    color: #ffffff;
    cursor: pointer;
  }
  
  .logo {
    /* Estilos para el logo */
    color: #ffffff;
  }
  
  .navbar-search {
    /* Estilos para la barra de búsqueda */
    color: #ffffff;
  }
  
  .navbar-config {
    /* Estilos para el icono de configuración */
    color: #ffffff;
  }
  
  .navbar-icons {
    display: flex;
    align-items: center;
    color: #ffffff;
  }
  
  .navbar-icons i {
    margin-right: 10px; /* Espacio entre los iconos */
  }
  
  .navbar-user {
    /* Estilos para la sección de nombre de usuario */
    color: #ffffff;
  }
  </style>
  
<template>
    <nav class="navbar-f">
      <div class="navbar-menu">
        <div class="menu-icon">
            <i class="fas fa-bars"></i>
            <h1>Dashboard  /</h1>
          <!-- Puedes utilizar alguna biblioteca de iconos como FontAwesome o un icono personalizado -->
        </div>
        <!-- <div class="logo">
            <h1>LOGO</h1>
          
        </div> -->
      </div>
      
    </nav>
  </template>

<!-- <script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  // Configuración del componente
});
</script> -->
  
  <style>
  .navbar-f {
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: fixed;
    top: 100px;
    left: 0;
    right: 0;
    height: 50px;
    background-color: rgb(56, 56, 73);
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 20px;
    /* Estilos adicionales para el navbar */
  }
  
  .navbar-menu {
    display: flex;
    align-items: center;
    /* Estilos adicionales para el menú */
  }
  
  .menu-icon {
    /* Estilos para el icono de menú de 3 rayas */
  }
  
  .logo {
    /* Estilos para el logo */
  }
  
  
  </style>
  
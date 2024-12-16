<template>
  <header class="header">
  <h1>Construtora Vieira</h1>
  <!-- Botão Hambúrguer -->
  <button class="hamburger" @click="toggleMenu">
  &#9776; <!-- Ícone de hambúrguer -->
  </button>
  <!-- Menu de Navegação -->
  <nav>
  <ul :class="['nav-links', { show: isMenuOpen }]">
  <li><a href="#home" @click="closeMenu">Home</a></li>
  <li><a href="#services" @click="closeMenu">Serviços</a></li>
  <li><a href="#projects" @click="closeMenu">Projetos</a></li>
  <li><a href="#contact" @click="closeMenu">Contato</a></li>
  </ul>
  </nav>
  </header>
  </template>
  
  <script>
  export default {
  name: "MainHeader",
  data() {
  return {
  isMenuOpen: false, // Estado inicial do menu
  };
  },
  methods: {
  toggleMenu() {
  this.isMenuOpen = !this.isMenuOpen; // Alterna o estado do menu
  console.log("isMenuOpen:", this.isMenuOpen); // Depuração
  },
  closeMenu() {
  this.isMenuOpen = false; // Fecha o menu ao clicar em um link
  },
  },
  };
  </script>
  
  <style scoped>
  /* Estilo do Header */
  .header {
  background-color: #004d40;
  color: white;
  padding: 20px;
  text-align: center;
  position: relative; /* Necessário para posicionar o botão */
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-sizing: border-box;
  }
  
  h1 {
  margin: 0;
  font-size: 1.5rem;
  }
  
  /* Menu em telas grandes */
  ul {
  list-style: none;
  display: flex;
  justify-content: center;
  padding: 0;
  margin: 0;
  }
  
  li {
  margin: 0 15px;
  }
  
  a {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  transition: color 0.3s ease;
  }
  
  a:hover {
  color: #ffcc00;
  }
  
  /* Botão Hambúrguer (apenas para telas pequenas) */
  .hamburger {
  display: none;
  background: none;
  border: none;
  font-size: 30px;
  color: white;
  cursor: pointer;
  position: absolute;
  top: 20px;
  right: 20px;
  z-index: 101;
  }
  
  /* Media Query para telas menores */
  @media (max-width: 768px) {
  .header {
  justify-content: space-between;
  }
  
  h1 {
  font-size: 1.2rem;
  }
  
  .nav-links {
  display: flex;
  flex-direction: column;
  position: fixed;
  top: 60px; /* Posicionado logo abaixo do header */
  left: 0;
  background-color: #9C915A;
  width: 100%;
  height: auto; /* Ajustado para não ocupar a tela toda */
  padding: 10px 0;
  text-align: center;
  box-sizing: border-box;
  z-index: 100;
  transform: translateX(-100%); /* Inicialmente escondido */
  transition: transform 0.3s ease-in-out;
  }
  
  /* Mostra o menu */
  .nav-links.show {
  display: flex;
  transform: translateX(0);
  }
  
  
  }
  
  @media (max-width: 480px) {
  .header {
  flex-direction: row;
  align-items: center;
  }
  
  .nav-links a {
  font-size: 0.9rem;
  padding: 10px 0;
  }
  
  li {
  margin: 5px 0;
  }
  }
  </style>
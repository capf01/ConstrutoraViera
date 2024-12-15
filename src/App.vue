<template>
  <div id="app">
    <!-- Componente Header -->
    <MainHeader />    
    <!-- Seção de Serviços -->
    <section>
      <h2>Nossos Serviços</h2>
      <OfferedServices />
    </section>
    <!-- Seção de Projetos -->
    <section>
      <h2>Nossos Projetos</h2>
      <UserProjects />
    </section>
    <!-- Componente ContactForm -->
    <div id="app">
    <ContactForm />
     <!-- Componente s -->
    <div>
    <SobreNos/>
    </div>
    <div>
      <ComoNosEncontrar/>
    </div>
  </div>
    <!-- Componente Footer -->
    <SiteFooter />
  </div>

</template>

<script>
// Importação dos componentes
import MainHeader from "./components/MainHeader.vue";
import SiteFooter from "./components/SiteFooter.vue";
import UserProjects from "./components/UserProjects.vue";
import OfferedServices from "./components/OfferedServices.vue";
import ContactForm from "./components/ContactForm.vue";
import SobreNos from "./components/SobreNos.vue";
import ComoNosEncontrar from "./components/ComoNosEncontrar.vue";
export default {
  name: "App",
  components: {
    MainHeader,
    SiteFooter,
    UserProjects,
    OfferedServices,
    ContactForm,
    SobreNos,
    ComoNosEncontrar
  },
  
};

</script>

<style>
/* Estilos globais (opcional) */
body {
  margin: 0;
   font-family: Arial, sans-serif;
  background-color: #f9f9f9;
}

section {
  margin: 20px;
  padding: 20px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

h2 {
  color: #004d40;
  margin-bottom: 15px;
}

</style>

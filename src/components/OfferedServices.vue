<template>
  <section id="services" class="section">
    <h2>Nossos Serviços</h2>
    <p>Construção civil, projetos arquitetônicos e reformas.</p>
    <div class="image-container">
      <!-- A imagem carregada dinamicamente -->
      <img :src="imageUrl" alt="Imagem de Serviços" />
      <img :src="imageUrl2" alt="Imagem de Serviços" />
      <img :src="imageUrl3" alt="Imagem de Serviços" />
    </div>
  </section>
</template>

<script>
export default {
  name: "OfferedServices",
  data() {
    return {
      imageUrl: require("@/assets/Images/Image1.jpeg"),
      imageUrl2: require("@/assets/Images/image2.jpeg"), // Caminho correto para a imagem
      imageUrl3: require("@/assets/Images/image3.jpeg"), // Caminho correto para a imagem
    };
  },
};
</script>

<style scoped>
.section {
  padding: 20px;
  background-color: #e0f2f1;
  margin: 20px 0;
  text-align: center;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.image-container {
  margin-top: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px; /* Espaçamento entre as imagens */
}

.image-container img {
  width: 100%;
  max-width: 400px;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

@media (max-width: 768px) {
  .image-container {
    flex-direction: column; /* Organiza as imagens verticalmente em telas menores */
  }

  .image-container img {
    max-width: 100%; /* Ajusta a largura das imagens em telas menores */
    margin-bottom: 15px; /* Adiciona um espaçamento entre as imagens */
  }
}
</style>

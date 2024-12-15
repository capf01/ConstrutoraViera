<template>
  <section id="projects" class="section">
    <div class="content">
      <h2>Sobre Nós</h2>
      <p>✨ Executamos seu projeto sem dor de cabeça!</p>
      <p>Vieira Construtora e Incorporadora</p>
      <p>💡 + de 100 mil m² executados</p>
    </div>
  </section>
</template>

<script>
export default {
  name: "SobreNos",
};
</script>

<style scoped>
.section {
  padding: 40px;
  background-color: #004d40; /* Cor de fundo em verde escuro */
  color: white;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  margin: 20px 0;
}

.content {
  text-align: center;
}

h2 {
  font-size: 32px;
  font-weight: bold;
  margin-bottom: 20px;
  color: #fff;
}

p {
  font-size: 18px;
  margin: 10px 0;
  line-height: 1.5;
}

p:first-of-type {
  font-size: 20px;
  color: #ffeb3b; /* Cor amarela para destacar */
}

p:last-of-type {
  font-size: 18px;
  color: #81c784; /* Cor verde suave */
}

@media (max-width: 768px) {
  .section {
    padding: 20px;
  }

  h2 {
    font-size: 28px;
  }

  p {
    font-size: 16px;
  }
}
</style>

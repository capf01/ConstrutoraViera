<template>
  <section id="projects" class="section">
    <div class="content">
      <h2>Sobre Nós</h2>
      <p>Na <strong>Vieira Construtora</strong>, transformamos sonhos em realidade com compromisso, qualidade e responsabilidade. Com mais de 5 anos de experiência no mercado da construção civil, somos especialistas em planejar, gerenciar e executar projetos que superam expectativas.</p>
      <p>Nosso foco é oferecer soluções completas e personalizadas, garantindo que cada projeto seja entregue no prazo, dentro do orçamento e com excelência. Desde a concepção inicial até a entrega final, cuidamos de cada detalhe para que você possa aproveitar o melhor da sua obra, sem preocupações com custos ou prazos excessivos.</p>
      <p>Somos movidos pelo desejo de construir lares e espaços que fazem a diferença na vida das pessoas, priorizando conforto, funcionalidade e estética. Nosso compromisso é simplificar sua jornada na construção, oferecendo suporte completo e transparente em cada etapa do processo.</p>
      
      <h3>Missão</h3>
      <p>Proporcionar uma experiência tranquila e satisfatória na construção, entregando obras que combinam qualidade, inovação e atendimento personalizado.</p>
      
      <h3>Visão</h3>
      <p>Ser referência em construção civil, reconhecida por realizar obras de excelência e criar relacionamentos de confiança com nossos clientes e parceiros.</p>
      
      <h3>Valores</h3>
      <ul>
        <li>✅ Compromisso com prazos e qualidade</li>
        <li>✅ Transparência em todos os processos</li>
        <li>✅ Respeito aos sonhos e necessidades dos clientes</li>
        <li>✅ Inovação e busca constante por melhorias</li>
      </ul>
      <p>Na <strong>Vieira Construtora</strong>, construímos mais do que paredes: construímos histórias e realizações. Conte conosco para transformar seu projeto no espaço ideal para viver, investir ou realizar!</p>
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
  font-family: 'Poppins', sans-serif;
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

h3 {
  font-size: 24px;
  margin-top: 20px;
  color: #ffeb3b;
}

p {
  font-size: 18px;
  margin: 10px 0;
  line-height: 1.5;
}

ul {
  list-style: none;
  padding: 0;
  margin: 20px 0;
}

li {
  font-size: 18px;
  margin: 5px 500px;
  color: #81c784; /* Cor verde suave */
  text-align: left;

}

p:first-of-type {
  font-size: 20px;
  color: #ffeb3b; /* Cor amarela para destacar */
}

@media (max-width: 768px) {
  .section {
    padding: 20px;
  }

  h2 {
    font-size: 28px;
  }

  h3 {
    font-size: 22px;
  }

  p, li {
    font-size: 16px;
  }
}
</style>

<template>  
  <section id="contact" class="section">
    <div class="contact-info">
      <h2>Como Nos Encontrar</h2>
      <p>Estamos localizados em Goiatuba, GO. Veja nossa localização no mapa e entre em contato.</p>
      
      <div class="map-container">
        <iframe
          width="100%"
          height="300"
          src="https://www.google.com/maps/embed/v1/place?q=Avenida+Presidente+Vargas+668A,+Goiatuba-GO&key=AIzaSyDHZCPY-nZ3vozFF32STNyGywCeUoF5b1w"
          frameborder="0"
          style="border:0"
          allowfullscreen
        ></iframe>
      </div>
      
      <div class="contact-details">
        <p><strong>Endereço:</strong> Avenida Presidente Vargas 668A, Goiatuba-GO, Centro, 75600-000.</p>
        <p><strong>Telefone:</strong> +55 62 99381-8441</p>
        <p><strong>Email:</strong> contato@viera.com</p>
      </div>

      <div class="contact-form">
        <h3>Envie uma mensagem:</h3>
        <form @submit.prevent="submitForm">
          <input type="text" v-model="name" placeholder="Seu Nome" required />
          <input type="email" v-model="email" placeholder="Seu Email" required />
          <textarea v-model="message" placeholder="Sua Mensagem" required></textarea>
          <button type="submit">Enviar</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContactUs",
  data() {
    return {
      name: "",
      email: "",
      message: "",
    };
  },
  methods: {
    submitForm() {
      alert(`Mensagem de ${this.name} foi enviada!`);
      this.name = "";
      this.email = "";
      this.message = "";
    },
  },
};
</script>

<style scoped>
.section {
  padding: 40px;
  background-color: #f9f9f9;
  margin: 20px 0;
  text-align: center;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.contact-info {
  max-width: 800px;
  margin: 0 auto;
}

h2 {
  font-size: 32px;
  margin-bottom: 20px;
}

p {
  font-size: 18px;
  margin-bottom: 20px;
}

.map-container {
  margin-bottom: 20px;
  border-radius: 8px;
  overflow: hidden;
}

.contact-details p {
  font-size: 18px;
  margin: 10px 0;
}

.contact-form {
  margin-top: 30px;
}

.contact-form h3 {
  font-size: 24px;
  margin-bottom: 10px;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 10px;
  margin-bottom: 10px;
  border-radius: 5px;
  border: 1px solid #ccc;
  font-size: 16px;
}

.contact-form button {
  background-color: #004d40;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
}

.contact-form button:hover {
  background-color: #00796b;
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

<template>
    <section id="contact" class="section">
      <h2>Entre em Contato</h2>
      <form @submit.prevent="submitForm">
        <!-- Campo Nome -->
        <label for="name">Nome:</label>
        <input
          type="text"
          id="name"
          v-model="name"
          placeholder="Seu nome"
        />
        <span v-if="errors.name" class="error">{{ errors.name }}</span>
  
        <!-- Campo Email -->
        <label for="email">Email:</label>
        <input
          type="email"
          id="email"
          v-model="email"
          placeholder="seuemail@exemplo.com"
        />
        <span v-if="errors.email" class="error">{{ errors.email }}</span>
  
        <!-- Campo Mensagem -->
        <label for="message">Qual tipo de serviço:</label>
        <textarea
          id="message"
          v-model="message"
          placeholder="Pode nos dar mais detalhes para o tipo de serviço que deseja?"
          rows="5"
        ></textarea>
        <span v-if="errors.message" class="error">{{ errors.message }}</span>
  
        <!-- Botão de Envio -->
        <button type="submit">Enviar</button>
  
        <!-- Mensagem de sucesso -->
        <p v-if="formSubmitted" class="success-message">
          Redirecionando para o WhatsApp...
        </p>
      </form>
    </section>
    
  <div class="image-container">
   <a href="https://api.whatsapp.com/send?phone=62993818441">
    <img :src="imageUrl" alt="Imagem do WhatsApp" />
  </a> </div>

  </template>
  
  <script>
  export default {
    name: "ContactForm",
    data() {
      return {
        name: "",
        email: "",
        message: "",
        errors: {},
        formSubmitted: false,
        imageUrl: "https://play-lh.googleusercontent.com/bYtqbOcTYOlgc6gqZ2rwb8lptHuwlNE75zYJu6Bn076-hTmvd96HH-6v7S0YUAAJXoJN",
      };
    },
    methods: {
      validateForm() {
        this.errors = {}; // Limpar erros anteriores
        let isValid = true;
  
        // Validação do campo Nome
        if (!this.name.trim()) {
          this.errors.name = "O nome é obrigatório.";
          isValid = false;
        }
  
        // Validação do campo Email
        const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        if (!this.email.trim()) {
          this.errors.email = "O email é obrigatório.";
          isValid = false;
        } else if (!emailRegex.test(this.email)) {
          this.errors.email = "Informe um email válido.";
          isValid = false;
        }
  
        // Validação do campo Mensagem
        if (!this.message.trim()) {
          this.errors.message = "A mensagem não pode estar vazia.";
          isValid = false;
        }
  
        return isValid;
      },
      submitForm() {
        if (this.validateForm()) {
          this.formSubmitted = true;
  
          // Número do WhatsApp e criação da mensagem formatada
          const whatsappNumber = "556293818441";
          const textMessage = `Olá, meu nome é ${this.name}. Meu email é ${this.email}. Gostaria do seguinte Serviço poderia me ajuadar?: "${this.message}"`;
  
          // Gerar URL do WhatsApp com os dados do formulário
          const whatsappURL = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(
            textMessage
          )}`;
  
          // Redirecionar o usuário para o WhatsApp
          window.open(whatsappURL, "_blank");
  
          // Resetar os campos do formulário
          this.name = "";
          this.email = "";
          this.message = "";
          setTimeout(() => (this.formSubmitted = false), 3000);
        }
      },
    },
  };
  </script>
  
  <style scoped>
  .section {
    padding: 20px;
    max-width: 600px;
    margin: 0 auto;
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  
  h2 {
    text-align: center;
    margin-bottom: 15px;
    color: #004d40;
  }
  
  form {
    display: flex;
    flex-direction: column;
  }
  
  label {
    margin-top: 10px;
    font-weight: bold;
  }
  
  input,
  textarea {
    padding: 8px;
    margin-top: 5px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  input:focus,
  textarea:focus {
    border-color: #00796b;
    outline: none;
  }
  
  button {
    margin-top: 15px;
    padding: 10px;
    background-color: #004d40;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #00796b;
  }
  
  .error {
    color: red;
    font-size: 12px;
  }
  
  .success-message {
    margin-top: 15px;
    color: green;
    text-align: center;
  
  }

  .image-container {
    display: flex;
    justify-content: right;
    align-items: center;
    margin-top: 20px;
  }

  .image-container img {
     position: fixed; 
    bottom: 20px;
    right: 20px;
    width: 65px;
    height: 65px;
    border-radius: 50%;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  </style>
  
<template>
    <div class="contact-page">
      <main class="main-content">
        <section class="contact-section">
          <h1>Contact Us</h1>
          <form @submit.prevent="submitForm">
            <div class="form-group">
              <label for="name">Nama:</label>
              <input type="text" id="name" v-model="form.name" required />
            </div>
            <div class="form-group">
              <label for="email">Email:</label>
              <input type="email" id="email" v-model="form.email" required />
            </div>
            <div class="form-group">
              <label for="message">Pesan:</label>
              <textarea id="message" v-model="form.message" required></textarea>
            </div>
            <button type="submit">Kirim Pesan</button>
          </form>
        </section>
      </main>
    </div>
</template>
  
<script setup>
  import { ref } from "vue";
  
  const form = ref({
    name: "",
    email: "",
    message: "",
  });
  
  const submitForm = () => {
    alert(
      `Terimakasih untuk pesannya, ${form.value.name}! Kami akan respon secepat mungkin!`
    );
    form.value.name = "";
    form.value.email = "";
    form.value.message = "";
  };
</script>
  
<style scoped>
  .contact-page {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    font-family: "Arial, sans-serif";
    background-color: #f9f9f9;
  }
  
  .main-content {
    flex: 1;
    width: 100%;
    max-width: 800px;
    padding: 20px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    background-color: #fff;
  }
  
  .contact-section {
    text-align: center;
  }
  
  .contact-section h1 {
    font-size: 2.5em;
    margin-bottom: 20px;
    color: #333;
  }
  
  .form-group {
    margin-bottom: 20px;
    text-align: left;
  }
  
  .form-group label {
    display: block;
    margin-bottom: 5px;
    font-size: 1em;
    color: #666;
  }
  
  .form-group input,
  .form-group textarea {
    width: 100%;
    padding: 10px;
    font-size: 1em;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  .form-group textarea {
    height: 150px;
  }
  
  button {
    padding: 10px 20px;
    font-size: 1em;
    background-color: #42b983;
    border: none;
    color: #fff;
    cursor: pointer;
    border-radius: 4px;
  }
  
  button:hover {
    background-color: #369f75;
  }
</style>
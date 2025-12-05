<script setup>
import { ref } from 'vue';

const countries = ['Brasil', 'Australia', 'Japão'];
const form = ref({
  name: '',
  message: '',
  country: ''
});
</script>

<template>
  <div class="container">

    <div class="box">
      <div class="form-group">
        <label>Nome</label>
        <input v-model="form.name" type="text" class="input">
      </div>

      <div class="form-group">
        <label>Mensagem</label>
        <textarea v-model="form.message" class="textarea"></textarea>
      </div>
      
      <div class="form-group">
        <label>País</label>
        <select v-model="form.country" value="country" class="selected">
          <option value="">Selecione um pais</option>
          <option v-for="country in countries" :key="country">{{ country }}</option>
        </select>
      </div>
    </div>

    <div class="preview">
      <h3>Pré-visualização</h3>
      <p><strong>Nome:</strong> {{ form.name }}</p>
      <p><strong>Mensagem:</strong> {{ form.message }}</p>
      <p><strong>País:</strong> {{ form.country }}</p>
    </div>

  </div>
</template>

<style>
/* Layout geral */
.container {
  width: 100%;
  max-width: 900px;
  margin: 40px auto;
  font-family: Arial, sans-serif;
  color: #e5e5e5; /* texto claro */
}

/* Caixa do formulário */
.box {
  padding: 20px;
  background: #1e1e1e;  /* fundo escuro */
  border-radius: 10px;
  border: 1px solid #333;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

/* Labels */
label {
  font-weight: bold;
  margin-bottom: 6px;
  color: #f0f0f0;
}

/* Inputs e textarea */
.input,
.selected,
.textarea {
  padding: 10px;
  background: #2a2a2a; /* mais escuro */
  border: 1px solid #444;
  border-radius: 6px;
  font-size: 16px;
  color: #fff;
  outline: none;
}

.input:focus,
.selected:focus,
.textarea:focus {
  border-color: #6aa9ff;
  box-shadow: 0 0 4px rgba(106, 169, 255, 0.6);
}

/* Textarea */
.textarea {
  min-height: 100px;
  resize: vertical;
}

/* Preview */
.preview {
  margin-top: 30px;
  padding: 20px;
  background: #262626;
  border-radius: 10px;
  border: 1px solid #333;
}

.preview h3 {
  margin-bottom: 10px;
  color: #bfbfbf;
}

.preview strong {
  color: #fff;
}
</style>

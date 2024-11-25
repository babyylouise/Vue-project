<script setup>
defineProps({
  schoolName: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="school-container">
    <header class="school-header">
      <h1>{{ schoolName }}</h1>
    </header>
    <main class="school-content">
      <p>Bem-vindo à nossa plataforma educacional!</p>
      <div class="actions">
        <router-link to="/professor" class="btn">Área do Professor</router-link>
        <router-link to="/aluno" class="btn">Área do Aluno</router-link>
      </div>
    </main>
  </div>
</template>

<style scoped>
.school-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  background: linear-gradient(135deg, #4a90e2, #50c9c3);
  color: white;
  font-family: Arial, sans-serif;
}

.school-header h1 {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 20px;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.4);
}

.school-content p {
  font-size: 1.5rem;
  margin-bottom: 30px;
  text-align: center;
}

.actions {
  display: flex;
  gap: 20px;
}

.btn {
  text-decoration: none;
  padding: 10px 20px;
  background-color: #1d3557;
  border-radius: 5px;
  color: white;
  font-size: 1.2rem;
  font-weight: bold;
  transition: transform 0.3s, background-color 0.3s;
}

.btn:hover {
  background-color: #457b9d;
  transform: scale(1.1);
}
</style>

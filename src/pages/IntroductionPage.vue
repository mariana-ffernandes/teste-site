<template>
  <div class="introduction-page">
    <header class="header-container">
      <router-link to="/menu" class="back-button">← voltar</router-link> 
      <h1 class="title">Introdução ao Conteúdo</h1>
    </header>
    <main>
      <div class="buttons-container">
        <button class="button-perda-auditiva" @click="showUnderConstructionMessage">O que é a perda auditiva?</button>
        <button class="button-funcao-aparelho" @click="showUnderConstructionMessage">Qual a função do aparelho auditivo?</button>
      </div>
    </main>
  </div>
</template>

<script>
import { mapState } from 'vuex';

export default {
  name: 'IntroductionPage',
  computed: {
    ...mapState(['userType'])
  },
  methods: {
    showUnderConstructionMessage() {
      alert('O conteúdo está sendo elaborado. Volte para a página de menu inicial.');
      this.$router.push('/menu');
    }
  }
}
</script>

<style scoped>
.introduction-page {
  text-align: center;
  padding: 20px;
}

.header-container {
  display: flex;
  justify-content: center;
  position: relative;
}

.back-button {
  position: absolute;
  left: 20px;
  font-family: 'Montserrat', sans-serif;
  font-size: 1.2rem;
  font-weight: 600;
  padding: 8px 20px;
  background-color: var(--color-white);
  color: var(--color-black);
  border: none;
  cursor: pointer;
  box-shadow: 5px 5px 1px -1px var(--color-text-top);
  text-align: center;
}

.title {
  font-family: 'Montserrat', sans-serif;
  font-weight: 600;
  font-size: 2rem;
  color: var(--color-text-top);
  margin: 20px auto;
}

.buttons-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
  max-width: 80%;
  margin: 0 auto;
}

.button-perda-auditiva,
.button-funcao-aparelho {
  background-color: var(--color-container-button);
  border: none;
  color: var(--color-black);
  font-family: 'Montserrat', sans-serif;
  font-size: 2.5rem;
  font-weight: 500;
  padding: 10px;
  width: 25rem;
  height: 13rem;
  cursor: pointer;
  align-items: center;
}

main {
  padding: 20px;
}

.content {
  font-size: 2rem;
  font-weight: 400;
  margin-top: 20px;
  color: var(--color-black);
}

.exit-button {
  font-family: 'Montserrat', sans-serif;
  font-size: 1rem;
  font-weight: 600;
  margin-top: 20rem;
  padding: 8px 20px;
  background-color: var(--color-background);
  color: var(--color-black);
  border: none;
  cursor: pointer;
  box-shadow: 5px 5px 1px -1px var(--color-text-top);
}

@media (max-width: 768px) {
  .title {
    margin-top: 100px;
    font-size: 2rem;
  }

  .back-button {
    font-size: 1.5rem; 
  }

  .buttons-container {
    flex-direction: column;
    gap: 15px;
  }

  .button-perda-auditiva,
  .button-funcao-aparelho {
    font-size: 2rem;
    width: 90%;
    height: 10rem;
    align-self: center;
  }
}

@media (max-width: 480px) {
.header-container {
  padding: 0px;
}

  .title {
    font-size: 1.5rem;
    margin-top: 100px;
  }

  .back-button {
    font-size: 1rem; 
  }

  .buttons-container{    
    padding: 0px 5px;
    align-items: center;
  }

  .button-perda-auditiva,
  .button-funcao-aparelho {
    margin-top: 0px;
    padding: 10px;
    font-size: 1.5rem;
  }
}
</style>

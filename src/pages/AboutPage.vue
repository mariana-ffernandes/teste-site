<template>
  <div class="about-page">
    <header class="header-container">
      <div class="logo-title-container">
        <img src="@/assets/logoProAASI.png" alt="ProAASI Logo" class="logo" />
        <h1 class="header-title">ProAASI</h1>
      </div>
      <h1 class="title">Sobre o ProAASI</h1>
    </header>
    <main class="main-container">
      <p class="content">
        Este conteúdo está sendo elaborado.
      </p>
    </main>
  </div>
</template>

<script>
export default {
  name: 'AboutPage'
}
</script>

<style scoped>
.about-page {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.header-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: transparent;
  padding: 20px;
}

.logo-title-container {
  display: flex;
  align-items: center;
}

.logo {
  width: 90px;
  margin-top: 70px;
}

.header-title {
  color: var(--color-black);
  font-family: 'Montserrat', sans-serif;
  font-size: 3rem;
  font-weight: 500;
  margin-left: 10px;
  margin-top: 70px;
}

.title {
  color: var(--color-container-success);
  font-family: 'Montserrat', sans-serif;
  font-size: 2rem;
  margin-top: 60px;
}

.main-container {
  flex: 1;
  padding: 10px;
}

.content {
  width: 90%;
  margin: 0 auto;
  font-family: 'Montserrat', sans-serif;
  font-size: 1.5rem;
  line-height: 1.6;
  color: var(--color-text-container);
}

.back-button {
  font-family: 'Montserrat', sans-serif;
  width: 20rem;
  height: 3rem;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: var(--color-white);
  color: var(--color-black);
  padding: 10px 10px;
  text-decoration: none;
  font-size: 1.2rem;
  font-weight: 500;
  border-radius: 0px;
  box-shadow: 2px 3px 1px 1px var(--color-shadow-button);
  cursor: pointer;
  transition: background-color 0.3s, color 0.3s;
}

.back-button:hover {
  background-color: var(--color-background);
  color: #333;
}
</style>

<template>
    <div class="importance-page">
      <h1>A importância de preencher o forms</h1>
      <br>
      <p>
        Preencher o formulário é uma etapa fundamental para o sucesso da nossa pesquisa de projeto. 
        Sua contribuição é essencial para que possamos coletar dados relevantes e precisos, que ajudarão a aprimorar nossos serviços e a entender melhor as necessidades dos usuários.
      </p>
      <br>
      <p>
        Ao preencher o formulário, você está contribuindo para um processo mais eficiente e eficaz.
    </p>
    <br>
    <h3>Agradecemos sua colaboração!</h3>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ImportanceOfFillingForms'
  }
  </script>
  
  <style scoped>
  .importance-page {
    padding: 20px;  
    padding-bottom: 310px;  
    font-family: 'Montserrat', sans-serif;
  }
  
  h1 {
    font-family: 'Montserrat', sans-serif;
    font-size: 2rem;
    color: var(--color-black);
  }
  
  p {
    font-family: 'Montserrat', sans-serif;
    font-size: 1.2rem;
    color: var(--color-black);
  }
  
  h3 {
    font-family: 'Montserrat', sans-serif;
    margin: 10px 0;
  }

  @media (max-width: 1024px){
    .importance-page {
    padding: 20px;
    padding-bottom: 440px;
    font-family: 'Montserrat', sans-serif;
  }
  
  h1 {
    font-family: 'Montserrat', sans-serif;
    font-size: 2rem;
    color: var(--color-black);
  }
  
  p {
    font-family: 'Montserrat', sans-serif;
    font-size: 1.2rem;
    color: var(--color-black);
  }
  
  h3 {
    font-family: 'Montserrat', sans-serif;
    margin: 10px 0;
  }    
  }

  @media (max-width: 768px){
    .importance-page {
    padding: 20px;
    padding-bottom: 150px;
    font-family: 'Montserrat', sans-serif;
  }
  
  h1 {
    font-family: 'Montserrat', sans-serif;
    font-size: 2rem;
    color: var(--color-black);
  }
  
  p {
    font-family: 'Montserrat', sans-serif;
    font-size: 1.2rem;
    color: var(--color-black);
  }
  
  h3 {
    font-family: 'Montserrat', sans-serif;
    margin: 10px 0;
  }    
  }

  @media (max-width: 480px){
    .importance-page {
    padding: 15px;    
    font-family: 'Montserrat', sans-serif;
  }
  
  h1 {
    font-family: 'Montserrat', sans-serif;
    font-size: 2rem;
    color: var(--color-black);
  }
  
  p {
    font-family: 'Montserrat', sans-serif;
    font-size: 1.2rem;
    color: var(--color-black);
  }
  
  h3 {
    font-family: 'Montserrat', sans-serif;
    margin: 10px 0;
  }    
  }
  </style>
  
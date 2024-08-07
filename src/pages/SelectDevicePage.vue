<template>
  <div class="select-device">
    <header>
      <router-link to="/menu" class="back-button">← voltar</router-link>
      <h1 class="title">Selecione o aparelho</h1>
    </header>
    <div class="devices-container">
      <div class="device" @click="selectDevice('intra-aural')">
        <img src="@/assets/icon_intraaural.png" alt="Descrição da Imagem" />
        <p>Mini<br>Intra-aural</p>
      </div>
      <div class="device" @click="selectDevice('mini-retro')">
        <img src="@/assets/icon_miniretro.png"/>
        <p>Mini Retro<br>com tubo fino</p>
      </div>
      <div class="device" @click="selectDevice('retroauricular-receptor')">
        <img src="@/assets/icon_retroauricular.png"/>
        <p>Mini<br>Retroauricular com receptor<br>no canal</p>
      </div>
      <div class="device" @click="selectDevice('retroauricular-molde')">
        <img src="@/assets/icon_retromolde.png"/>
        <p>Mini Retroauricular com molde</p>
      </div>
    </div>
    <button @click="exit" class="exit-button">Sair</button>
  </div>
</template>

<script>
import { mapMutations } from 'vuex';

export default {
  name: 'SelectDevicePage',
  methods: {
    ...mapMutations(['setSelectedDevice']),
    selectDevice(device) {
      this.setSelectedDevice(device);
      this.$router.push({ name: 'DeviceHandling' });
    },
    exit() {
      this.$router.push('/identification');
    }
  }
}
</script>

<style scoped>
.select-device {
  text-align: center;
  padding: 20px;
}

.back-button {
  font-family: 'Montserrat', sans-serif;
  font-size: 1.2rem;
  font-weight: 600;
  margin-top: 20px;
  padding: 8px 20px; 
  background-color: var(--color-background);
  color: var(--color-black)000;
  border: none;
  cursor: pointer;
  box-shadow: 5px 5px 1px -1px var(--color-text-top);    
  text-align: center;
  width: auto;
  position: absolute;
  top: 27%;
  left: 20px;
  margin: 10px;
}

.title {
  color: var(--color-text-top);
  font-family: 'Montserrat', sans-serif;
  font-size: 2rem;
  font-weight: 600;
  margin: 25px auto;
  text-align: center;
  width: fit-content;
}
  
.devices-container {
  background-color: var(--color-container-button);
  border: none;
  color: var(--color-black);
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 20px auto;
  width: 95%;
  height: 25rem;
}

.device {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 70px auto;
  cursor: pointer;
  width: 150px;
  word-wrap: break-word;
}

.device p {
  margin-top: 10px;
  color: var(--color-text-container);
  font-family: 'Montserrat', sans-serif;
  font-size: 1.3rem;
  font-weight: 500;
  text-align: center;
  white-space: normal;
}

.exit-button {
  font-family: 'Montserrat', sans-serif;
  font-size: 1rem;
  font-weight: 600;
  margin-top: 20px;
  padding: 8px 20px; 
  background-color: var(--color-background);
  color: var(--color-black)000;
  border: none;
  cursor: pointer;
  box-shadow: 5px 5px 1px -1px var(--color-text-top);
}

@media (max-width: 1024px) {
  .title {
    font-size: 1.8rem;
  }

  .device {
    width: 120px;
  }

  .device p {
    font-size: 1.2rem; 
  }

  .back-button,
  .exit-button {
    font-size: 1rem; 
  }
}

@media (max-width: 768px) {
  .title {
    font-size: 1.5rem;
  }

  .devices-container {
    height: auto; 
  }

  .device {
    width: 40%;
    margin: 30px;
  }

  .device p {
    font-size: 1.2rem; 
  }

  .back-button {
    font-size: 1.2rem;
    padding: 7px 15px; 
    margin-top: 20px;
  }
  .exit-button {
    font-size: 1.2rem; 
    padding: 7px 15px; 
  }
}

@media (max-width: 480px) {
  .title {
    margin-top: 60px;
    font-size: 1.2rem;
  }

  .back-button,
  .exit-button {
    font-size: 1rem; 
    padding: 7px 15px; 
  }

  .devices-container {
    flex-direction: column; 
    align-items: center; 
  }

  .device {
    width: 80%; 
    margin: 10px 0; 
  }

  .device p {
    font-size: 1rem;
  }
}
</style>
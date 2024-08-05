<!-- Imports -->
<script setup>
import { ref } from "vue";

const produto = ref(new URL("@/assets/Banana.png", import.meta.url).href);

const banana = () => {
  produto.value = new URL("@/assets/banana.png", import.meta.url).href;
};

const morango = () => {
  produto.value = new URL("@/assets/morango.png", import.meta.url).href;
};
const cobertura = () => {
  produto.value = new URL("@/assets/cobertura.png", import.meta.url).href;
};
</script>

<template>
  <section>
    <div class="container">
      <div class="information">
        <h1>Mais que café, Isso é <span>Starbucks!</span></h1>
        <p>
          As lojas Starbucks oferecem uma variedade de cafés coados do modo
          tradicional, alternados em intervalos de tempo (geralmente semanal,
          dependendo da disponibilidade dos grãos) para proporcionar aos
          clientes uma maneira fácil de experimentar seus diferentes cafés e
          blends.
        </p>
        <button>SAIBA MAIS</button>
      </div>

      <div class="view">
        <figure class="view__destaque">
          <img :src="produto" alt="milkshake" />
        </figure>

        <figure class="view__rede">
          <img src="../../assets/face.png" alt="Facebook" />
          <img src="../../assets/tt.png" alt="X" />
          <img src="../../assets/insta.png" alt="Instagram" />
        </figure>
      </div>
    </div>
  </section>

  <section class="produto">
    <img @click="banana" src="../../assets/Banana.png" alt="" />
    <img @click="morango" src="../../assets/morango.png" alt="" />
    <img @click="cobertura" src="../../assets/cobertura.png" alt="" />
  </section>
</template>

<style scoped>
section {
  display: flex;
  justify-content: center;
  height: 60vh;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 90vw;
}

.information {
  width: 50vw;
  max-width: 750px;
  height: 50vh;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

.information h1 {
  font-size: 3.5em;
  font-weight: 600;
}

.information span {
  color: #006439;
  font-weight: 800;
  font-size: 1.2em;
}

.information button {
  background-color: #006439;
  color: white;
  width: 10vw;
  height: 5vh;
  border: none;
  max-width: 120px;
  border-radius: 17px;
}

.view {
  height: 70vh;
  display: flex;
  align-items: center;
}

.view__destaque {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40vw;
  height: 50vh;
  max-width: 600px;
}
.view__destaque img {
  width: 100%;
  max-width: 300px;
  height: 35vh;
}

.view__rede {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  height: 20vh;
  background-color: #006439;
  padding: 0.5rem;
  border-radius: 10px;
}

.view__rede img {
  width: 5vw;
  max-width: 40px;
  height: 4vh;
  cursor: pointer;
}

.produto {
  height: 17vh;
}

.produto img {
  cursor: pointer;
}
</style>

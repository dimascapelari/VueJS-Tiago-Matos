<template>
  <div>
    Two-way data binding<br />
    v-model -> formulários
    <br />
    <br />
    <label>Nome</label><br />
    <input v-model="name" type="text" />
    <br />
    {{ name }}
  </div>

  <br />
  <br />

  <div>
    <label>Sports</label><br />
    <select v-model="sports">
      <option value="">Escolha</option>
      <option value="futebol">Futebol</option>
      <option value="skate">Skate</option>
      <option value="tenis">Tenis</option>
    </select>
    <br />
    {{ sports }}
  </div>

  <br />

  <div>
    <label>Newsletter</label><br />
    <input v-model="newsletter" type="radio" value="Sim" />Sim
    <input v-model="newsletter" type="radio" value="Não" />Não
    <br />
    {{ newsletter }}
  </div>

  <br />
  <br />

  <div>
    <label>Contrato</label><br />
    <input v-model="contract" type="checkbox" value="Sim" />Sim
    <br />
    Aceita nossos termos... <br />
    {{ contract }}
  </div>

  <br />
  <br />

  <div>
    <label>Cores que você mais gosta</label><br />
    <input v-model="colors" type="checkbox" value="Azul" />Azul
    <input v-model="colors" type="checkbox" value="Amarelo" />Amarelo
    <br />
    {{ colors }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Dimas Capelari",
      sports: "",
      newsletter: "",
      contract: false,
      colors: [],
    };
  },
};
</script>

<style></style>

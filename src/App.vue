<template>
  <div>
    <h2>Aula 13 - Componentes Slot</h2>
    <AulaTrezeComponentesSlot>
      <h3>Conteúdo inserido pelo Slot "default"</h3>

      <template v-slot:description>
        <p>Conteúdo inserido pelo Slot "description"</p>
      </template>

      <template v-slot:teste>
        <p>Conteúdo inserido pelo Slot "teste"</p>
      </template>
    </AulaTrezeComponentesSlot>
  </div>
  <hr />
  <h2>Aula 12 - Ciclo de Vida (File Cycle)</h2>
  <AulaDozeCicloDeVidaFileCycle />
  <hr />
  <h2>Aula 11 - Observadores (watch)</h2>
  <AulaOnzeObservadoresWatch />
  <hr />
  <h2>Aula 10 - Propriedade Computada (computed)</h2>
  <AulaDezPropriedadeComputada />
  <hr />
  <br />
  <h2>Aula 9 - Eventos</h2>
  <AulaNoveEventos />
  <br />
  <hr />
  <br />
  <br />
  <h2>Aula 8 - V-model</h2>
  <AulaOitoVmodel />
  <br />
  <hr />
  <h2>Aula 7 - Class e Style dinâmicos</h2>
  <AulaSeteClassStyle />
  <hr />

  <h2>Aula 5 e 6 V-for e V-bind</h2>
  <AulaCincoSeisVforVbind />
  <hr />

  <h2>Aula 4 - Condicionais</h2>
  <AulaQuatroCondicionais />
  <hr />

  <h2>Aula 3 - Componente Header</h2>
  <TheHeader v-if="showHeader" />
  <hr />
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import AulaNoveEventos from "./components/AulaNoveEventos.vue";
import AulaOitoVmodel from "./components/AulaOitoVmodel.vue";
import AulaSeteClassStyle from "./components/AulaSeteClassStyle.vue";
import AulaCincoSeisVforVbind from "./components/AulaCincoSeisVforVbind.vue";
import AulaQuatroCondicionais from "./components/AulaQuatroCondicionais.vue";
import AulaDezPropriedadeComputada from "./components/AulaDezPropriedadeComputada.vue";
import AulaOnzeObservadoresWatch from "./components/AulaOnzeObservadoresWatch.vue";
import AulaDozeCicloDeVidaFileCycle from "./components/AulaDozeCicloDeVidaFileCycle.vue";
import AulaTrezeComponentesSlot from "./components/AulaTrezeComponentesSlot.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    AulaTrezeComponentesSlot,
    AulaDozeCicloDeVidaFileCycle,
    AulaOnzeObservadoresWatch,
    AulaDezPropriedadeComputada,
    AulaNoveEventos,
    AulaOitoVmodel,
    AulaSeteClassStyle,
    AulaCincoSeisVforVbind,
    AulaQuatroCondicionais,
  },
  data() {
    return {
      showHeader: true,
    };
  },
};
</script>

<style>
.title {
  font-size: 20px;
  color: blue;
}

.title-home {
  font-size: 40px;
  color: green;
}

.text {
  color: red;
}

.text-home {
  color: greenyellow;
}

.todos-item {
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #fff;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

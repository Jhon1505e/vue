<template>
  <div class="row p-2">
    <span class="border border-primary border-3 opacity-75">
      <div class="col p-5">
        <h2 class="col p-3" style="color: #0288d1">Ingrese su tarea</h2>
        <div class="input-group mb-3">
          <input
            type="text"
            class="form-control"
            placeholder="Ingrese la tarea"
            aria-label="Recipient's username"
            aria-describedby="button-addon2"
            v-model="tarea"
          />
          <button
            class="btn btn-outline-primary"
            type="button"
            id="button-addon2"
            @click="ponerTarea"
            :disabled="tarea == ''"
          >
            Enviar
          </button>
        </div>
      </div>
      <hr class="border border-primary border-2 opacity-75" />
      <div class="col p-5">
        <h2 style="color: #0288d1">Tareas</h2>
        <hr />
        
        <p v-for="(t, i) in tareas" :key="i">
         <input type="checkbox">
           <span class="p-2">{{ t }}</span>
          <button @click="eliminarTarea(i)" class="btn btn-sm btn-danger">X</button>
        </p>
      </div>
    </span>
  </div>
</template>

<script>
export default {
  name: "Barra",

  data: () => ({
    tarea: "",
    tareas: [],
  }),

  methods: {
    ponerTarea() {
      this.tareas.push(this.tarea);
      this.tarea = "";
    },

    eliminarTarea(x) {
      this.tareas.splice(x, x + 1);
    },
  },
};
</script>
<style>
h2 {
  font-family: "Mochiy Pop One", sans-serif;
}
</style>
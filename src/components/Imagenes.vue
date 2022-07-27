<template>
  <div class="row">
    <div class="col pt-5">
      <div>
   <v-btn
      class="ma-2"
      outlined
      color=""
      v-model="sizes"
      @click="aumentarSize"
    >
      Disminuir Tamaño
    </v-btn>

    <v-btn
      class="m-2 m-3"
      outlined
      color="success"
      v-model="sizes"
      @click="aumentarSize"
    >
      Aumentar Tamaño
    </v-btn>
  </div>

      <v-slider
        style="color: #2196f3"
        v-model="size"
        hint="Im a hint"
        max="100"
        min="0"
      ></v-slider>
      {{ size }}
      <v-img
        class="img"
        lazy-src="https://picsum.photos/id/11/10/6"
        :max-height="size + '%'"
        :max-width="size + '%'"
        src="https://picsum.photos/id/11/500/300"
      ></v-img>
    </div>
    <div></div>
  </div>
</template>

<script>
export default {
  name: "Imagenes",

  data: () => ({
    size: 100,
    sizes: 10,
  }),

  methods: {
    aumentarSize() {
      
    },
    disminuirSize() {
      
    },
  },
};
</script>

<style>
.img {
  border: 2px solid #0288d1;
  border-radius: 50px;
  padding: 10px;
}

</style>
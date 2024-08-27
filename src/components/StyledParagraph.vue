<script>
export default {
  name: 'StyledParagraph',
  data() {
    return {
      color: 'blue',
      fondo: 'pink',
      borde: '3px solid black'
    }
  }
}
</script>
<template>
  <form>
    <label for="color">Color</label>
    <input type="text" id="color" v-model="color" />

    <label for="fondo">Colo de Fondo</label>
    <input type="text" id="fondo" v-model="fondo" />

    <label for="borde">Borde</label>
    <input type="text" id="borde" v-model="borde" />
  </form>
  <p :style="{ color: color, backgroundColor: fondo, border: borde }">Parrafo Estiloso 🔆</p>
  <p>Color: {{ color }}, fondo: {{ fondo }}, borde: {{ borde }}</p>
</template>
<style></style>

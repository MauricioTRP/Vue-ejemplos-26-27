<script>
export default {
  name: 'H1DosPuntoCero',
  data() {
    return {
      colores: ['pink', 'green', 'black', 'blue'],
      fondo: ''
    }
  }
}
</script>

<template>
  <h1 :style="{ background: fondo }" :class="{ 'text-white': fondo === 'black' }">
    Nuestro título camaleón
  </h1>
  <form>
    <select name="" v-model="fondo">
      <option v-for="(color, idx) in colores" :key="idx" :value="color">
        {{ color }}
      </option>
    </select>
  </form>
</template>

<style>
.text-white {
  color: white;
}
</style>

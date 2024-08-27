<script>
export default {
  name: 'H1Dinamico',
  data() {
    return {
      selectedClasses: [],
      posibleClasses: [
        { value: 'red', text: 'Texto rojo' },
        { value: 'blue', text: 'Fondo Azul' },
        { value: 'decoration', text: 'Subrayado' },
        { value: 'text-large', text: 'Texto Grande' },
        { value: 'text-light', text: 'Texto Liviano' }
      ]
    }
  }
}
</script>
<template>
  <h1 :class="selectedClasses">Mi Título con Clases 🚀🔪</h1>
  <form>
    <div v-for="clase in posibleClasses" :key="clase.value">
      <label :for="clase.value">{{ clase.text }}</label>
      <input type="checkbox" :id="clase.value" :value="clase.value" v-model="selectedClasses" />
    </div>
  </form>
</template>
<style scoped>
.red {
  color: red;
}
.blue {
  background-color: blue;
}

.decoration {
  text-decoration: underline;
}

.text-large {
  font-size: 40px;
}

.text-light {
  font-weight: 100;
}
</style>

<script>
export default {
  name: 'ClassReactive',
  data() {
    return {
      rotado: false,
      large: false
    }
  }
}
</script>
<template>
  <p
    :class="{
      alReves: rotado,
      textoGigante: large
    }"
  >
    🙀🙀🙀🙀
  </p>

  <form>
    <div>
      <label for="rotated">Rotado</label>
      <input type="checkbox" id="rotated" v-model="rotado" />
      <label for="large">large</label>
      <input type="checkbox" id="large" v-model="large" />
    </div>
  </form>
</template>
<style scoped>
.alReves {
  transform: rotate(180deg);
}

.textoGigante {
  font-size: 110px;
}
</style>

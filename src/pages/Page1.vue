<template>
  <q-page>
    <h1>hola soy nueva pagina</h1>
    <input type="text" v-model="nombre" />
    <br>
    {{nombre}} <br>
    <input type="number" v-model="num1">
    <input type="number" v-model="num2">
    {{num1+num2}}
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      nombre: "Juan perez",
      num1:4,
      num2:5
    };
  },
};
</script>

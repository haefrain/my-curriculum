<template>
  <div>
    <v-row>
      <v-col cols="12">
        <h2>{{pageTitle}}</h2>
      </v-col>
    </v-row>
  </div>
</template>
<script setup>
  const route = useRoute();
  const pathTitle = {'/': 'Resumen', '/experience': 'Experiencia', '/study': 'Estudios', '/hobbies': 'Hobbies', '/setup': 'Setup', '/tools': 'Herramientas'};
  const pageTitle = computed(() => {
    return pathTitle[route.path];
  })
</script>
<template>
  <div>
    <v-row justify="center" class="border-top-bottom ml-1 mr-1" >
      <v-col class="pt-0 pb-0">
        <NuxtLink to="/" class="n-link-base">
          Resumen
        </NuxtLink>
      </v-col>
      <v-col class="pt-0 pb-0">
        <NuxtLink to="/experience" class="n-link-base">
          Experiencia
        </NuxtLink>
      </v-col>
      <v-col class="pt-0 pb-0">
        <NuxtLink to="/study" class="n-link-base">
          Estudios
        </NuxtLink>
      </v-col>
      <v-col class="pt-0 pb-0">
        <NuxtLink to="/hobbies" class="n-link-base">
          Hobbies
        </NuxtLink>
      </v-col>
      <v-col class="pt-0 pb-0">
        <NuxtLink to="/setup" class="n-link-base">
          Setup
        </NuxtLink>
      </v-col>
      <v-col class="pt-0 pb-0">
        <NuxtLink to="/tools" class="n-link-base">
          Herramientas
        </NuxtLink>
      </v-col>
    </v-row>
  </div>
</template>
<style>
.border-top-bottom {
  border-top: 1px solid black;
  border-bottom: 1px solid black;
}
</style>
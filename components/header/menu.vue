<template>
  <div>
    <v-row justify="center" class="border-top-bottom ml-1 mr-1" >
      <v-col class="pt-2 pb-2 option-menu">
        <NuxtLink to="/" class="n-link-base">
          Resumen
        </NuxtLink>
      </v-col>
      <v-col class="pt-2 pb-2 option-menu">
        <NuxtLink to="/experience" class="n-link-base">
          Experiencia
        </NuxtLink>
      </v-col>
      <v-col class="pt-2 pb-2 option-menu">
        <NuxtLink to="/study" class="n-link-base">
          Estudios
        </NuxtLink>
      </v-col>      
      <v-col class="pt-2 pb-2 option-menu">
        <NuxtLink to="/hobbies" class="n-link-base">
          Hobbies
        </NuxtLink>
      </v-col>
      <v-col class="pt-2 pb-2 option-menu">
        <NuxtLink to="/setup" class="n-link-base">
          Setup
        </NuxtLink>
      </v-col>
    </v-row>
  </div>
</template>
<style scoped>
.option-menu > .n-link-base.router-link-active   {
  color: white;
  font-weight: bold;
  background: black;
  padding: 5px;  
}
.border-top-bottom {
  border-top: 1px solid black;
  border-bottom: 1px solid black;
}
.option-menu > .n-link-base {
  color: black;
  font-weight: bold;
  text-decoration: none;
  padding: 5px;
}
.option-menu > .n-link-base:hover {
  color: white;
  font-weight: bold;
  background: black;
}


</style>
<template>
  <div class="pb-2">
    <v-row justify="center" align="center" class="full-height">      
      <v-col cols="11" xs="11" sm="11" md="8" lg="6" xl="6" class="full-border">
        <Header />
        <NuxtPage/>
      </v-col>
    </v-row>
  </div>
</template>
<style>
  .full-border {   
    min-height: 95vh;
    border: 1px solid black;
  }

  .full-height {
    height: 95vh;
    margin-top: 20px;
  }
</style>

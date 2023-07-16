<template>
  <div>
    <v-row>
      <v-col cols="12" xs="12" sm="12" md="6" lg="6" xl="6" xxl="6">
        <v-card>
          <v-card-item>
            <v-card-title>Contactame</v-card-title>
          </v-card-item>

          <v-card-text>
            <v-row>
              <v-col>
                <div class="font-weight-bold d-inline-block mr-2">Teléfono:</div>
                <div class="d-inline-block">
                  <a href="tel:+573005093219" class="text-decoration-none font-color-black" target="_blank">+57 300 509 32 19</a>
                </div> 
                <br />
                <div class="font-weight-bold d-inline-block mr-2">Correo: </div>
                <div class="d-inline-block">
                  <a href="mailto:haefrain@gmail.com" class="text-decoration-none font-color-black" target="_blank">haefrain@gmail.com</a>
                </div> 
                <br />
                <div class="font-weight-bold d-inline-block mr-2">Ubicación: </div>
                <div class="d-inline-block">
                  <a href="https://www.google.com/maps/place/Ibagu%C3%A9,+Ibague,+Tolima/@4.4123739,-75.2279772,13z/data=!3m1!4b1!4m6!3m5!1s0x8e38c491115f4d5f:0xe0cae43859d2401e!8m2!3d4.444676!4d-75.242438!16zL20vMDU0aDNn?entry=ttu" class="text-decoration-none font-color-black" target="_blank">Ibague, Tolima, Colombia</a>
                </div>                 
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12" class="text-right">
                <a href="https://api.whatsapp.com/send?phone=573005093219&text=%C2%A1Hola!%20Te%20escribo%20desde%20tu%20sitio%20web" class="mr-2 font-color-black" target="_blank">
                  <v-icon icon="mdi-whatsapp" size="x-large"></v-icon>
                </a>
                <a href="https://www.linkedin.com/in/haefrain47/" class="mr-2 font-color-black" target="_blank">
                  <v-icon icon="mdi-linkedin" size="x-large"></v-icon>
                </a>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="12" xs="12" sm="12" md="6" lg="6" xl="6" xxl="6">
        <v-card>
          <v-card-item>
            <v-card-title>Acerca de</v-card-title>
          </v-card-item>

          <v-card-text>
            <v-row>
              <v-col class="text-justify">
                <p class="mb-2">El sitio web está hecho desarrollado con Nuxt 3 y desplegado en vercel, si pulsas el icono de Github veras el codigo fuente.</p>
                <small>Todos los textos que encontrarás aquí fueron generados por una IA a partir de mi curriculum y otra información recopilada en mis redes sociales.</small>
                
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12" class="text-right">
                <a href="https://drive.google.com/drive/folders/1yG6-LT6pEKUMM7Oc8I7x9gIBvw5dCwAj?usp=sharing" class="mr-2 font-color-black" target="_blank">
                  <v-icon icon="mdi-download" size="x-large"></v-icon>
                </a>
                <a href="https://github.com/haefrain/my-curriculum/" class="mr-2 font-color-black" target="_blank">
                  <v-icon icon="mdi-github" size="x-large"></v-icon>
                </a>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
        
      </v-col>
    </v-row>
  </div>
</template>
<style scoped>
.font-color-black {
  color: black;
}
</style>
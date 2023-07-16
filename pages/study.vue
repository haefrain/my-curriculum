<template>
  <div>
      <v-row>
          <v-col cols="12" v-if="isMobile">
            <TransversalCards :experience="experience" />            
          </v-col>
          <v-col cols="12" v-else>
            <TransversalTimeline :experience="experience" />
          </v-col>
      </v-row>
  </div>
</template>
<script>
const experience = ref([
  {
    years: "2015 - 2016",
    title: "Tecnologia Sinergia",
    url: "https://media.licdn.com/dms/image/C4E03AQFyVMtjhzIVew/profile-displayphoto-shrink_800_800/0/1667914331369?e=2147483647&v=beta&t=GZN73fjYxqAwFza7k8j2uJxtWAJIs7fr8byLwWJcjo8",
    position: "Desarrollador Junior",
    description: "Estuve a cargo de diseñar y desarrollar reportes personalizados para los clientes, utilizando herramientas como Crystal Reports y Jasper Reports. También me encargaba de optimizar las consultas SQL para mejorar el rendimiento de la base de datos MySQL, y de implementar nuevas funcionalidades en el módulo de inventarios del ERP Sihos Web, un sistema web desarrollado en PHP 5.6 con HTML, CSS y JavaScript con jQuery. Mi trabajo requería de un alto nivel de profesionalismo, responsabilidad y calidad, ya que los reportes y el módulo de inventarios eran esenciales para la gestión y el control de los recursos médicos y farmacéuticos de los clientes en su mayoría del sector público.",
    tags: ["PHP", "MySQL", "HTML", "CSS", "Javascript", "jQuery", "SQL", "Jasper Reports", "Crystal Reports"],
  },
])
export default {
  setup() {
    return {
      experience
    }
  },
  computed: {
    isMobile() {
      return this.$vuetify.display.xs || this.$vuetify.display.sm
    }
  }
}
</script>
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
      <v-row>
        <v-col>
          <StudyShortCourse :shortCourses="shortCourses" />
        </v-col>
      </v-row>
  </div>
</template>
<script>
const experience = ref([
  {
    years: "2007 - 2012",
    title: "Colegio los Andes de Ibague",
    url: "data:image/jpeg;base64,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",
    position: "Bachiller Academico con enfasis empresarial",
    description: "He cursado y aprobado el ciclo de educación media con una orientación hacia el desarrollo de competencias para la gestión de proyectos, la innovación y el emprendimiento.",
    tags: [],
  },
  {
    years: "2013 - 2015",
    title: "SENA",
    url: "https://lostramites.com.co/wp-content/uploads/logo-sena-fondo-naranja-300x300.jpg",
    position: "Tecnologo en Analisis y Desarrollo de Sistemas de Información",
    description: "Soy un tecnólogo en Análisis y Desarrollo de Sistemas de Información (ADSI) del SENA en Colombia. Mi formación me ha permitido adquirir las competencias necesarias para diseñar, desarrollar, implementar y mantener sistemas de información que respondan a las necesidades de las organizaciones. Me he especializado en el uso de diferentes lenguajes de programación, bases de datos, herramientas de desarrollo web y móvil, metodologías ágiles y estándares de calidad. Gracias a lo anterior mencionado me considero un profesional con capacidad de innovar, resolver problemas, trabajar en equipo y adaptarme a los cambios tecnológicos. Cabe resaltar que tuve doble mención de honor consecutiva y una tercera durante el grado como mejor aprendiz de la promoción.",
    tags: [],
  },
  {
    years: "2022 - Actual",
    title: "Fundacion de Educacion Superior San Jose",
    url: "https://media.licdn.com/dms/image/C4E0BAQFYc-z-ONr66w/company-logo_100_100/0/1631114992253?e=1697673600&v=beta&t=2o9y1kpbm4W5siZUB_GtADASKlQFqbWFx0t6iVSaRL0",
    position: "Ingeniero de Sistemas",
    description: "Un Ingeniero de Sistemas de la universidad san José es un profesional capacitado para diseñar, implementar y gestionar soluciones informáticas que respondan a las necesidades de diferentes sectores de la sociedad. Este título acredita el dominio de los fundamentos teóricos y prácticos de la ingeniería de software, las redes de comunicación, la inteligencia artificial, la seguridad informática y otras áreas relacionadas con el desarrollo y la innovación tecnológica. Un Ingeniero de Sistemas de la universidad san José también posee competencias para el trabajo en equipo, el liderazgo, la comunicación efectiva y el compromiso ético y social.",
    tags: [],
  },
])

const shortCourses = ref([
  {
    provider: "Platzi",
    url: "https://platzi.com/p/haefrain/curso/2793-computacion-basica/diploma/detalle/",
    url_image: "https://startupxplore.com/uploads/ff8080815235115101523595712a00de-large.png",
    title: "Computacion Basica",
    description: "",
    hours: "",
    year: "2022",
  },
  {
    provider: "Platzi",
    url: "https://platzi.com/p/haefrain/curso/1050-basico-programacion/diploma/detalle/",
    url_image: "https://startupxplore.com/uploads/ff8080815235115101523595712a00de-large.png",
    title: "Programacion Basica",
    description: "",
    hours: "",
    year: "2022",
  },
  {
    provider: "Platzi",
    url: "https://platzi.com/p/haefrain/curso/1945-ingles-principiantes/diploma/detalle/",
    url_image: "https://startupxplore.com/uploads/ff8080815235115101523595712a00de-large.png",
    title: "Short and Common Conversations",
    description: "",
    hours: "",
    year: "2022",
  },
  {
    provider: "Platzi",
    url: "https://platzi.com/p/haefrain/curso/2292-terminal/diploma/detalle/",
    url_image: "https://startupxplore.com/uploads/ff8080815235115101523595712a00de-large.png",
    title: "Introduccion a la terminal y linea de comandos",
    description: "",
    hours: "",
    year: "2022",
  },
  {
    provider: "Platzi",
    url: "https://platzi.com/p/haefrain/curso/2508-backend-introduccion/diploma/detalle/",
    url_image: "https://startupxplore.com/uploads/ff8080815235115101523595712a00de-large.png",
    title: "Introduccion al backend",
    description: "",
    hours: "",
    year: "2022",
  },
  {
    provider: "Platzi",
    url: "https://platzi.com/p/haefrain/curso/2633-estrategias-ingles/diploma/detalle/",
    url_image: "https://startupxplore.com/uploads/ff8080815235115101523595712a00de-large.png",
    title: "Estrategias para estudiar ingles",
    description: "",
    hours: "",
    year: "2022",
  },
  {
    provider: "Platzi",
    url: "https://platzi.com/p/haefrain/curso/1557-git-github/diploma/detalle/",
    url_image: "https://startupxplore.com/uploads/ff8080815235115101523595712a00de-large.png",
    title: "Git y Github",
    description: "",
    hours: "",
    year: "2022",
  },
  {
    provider: "Platzi",
    url: "https://platzi.com/p/haefrain/curso/1098-ingenieria/diploma/detalle/",
    url_image: "https://startupxplore.com/uploads/ff8080815235115101523595712a00de-large.png",
    title: "Fundamentos de Ingenieria de Software",
    description: "",
    hours: "",
    year: "2022",
  },
  {
    provider: "Udemy",
    url: "https://www.udemy.com/certificate/UC-ccd1d37e-33d6-4e6f-8d97-4a3edff661dd/",
    url_image: "https://logowik.com/content/uploads/images/udemy-new-20212512.jpg",
    title: "SOLID Principles: Introducing Software Architecture & Design",
    description: "",
    hours: "",
    year: "2022",
  },
  {
    provider: "SENA",
    url: "#",
    url_image: "https://lostramites.com.co/wp-content/uploads/logo-sena-fondo-naranja-300x300.jpg",
    title: "Basico de contabilidad, costos y presupuesto",
    description: "",
    hours: "",
    year: "",
  },
  {
    provider: "SENA",
    url: "#",
    url_image: "https://lostramites.com.co/wp-content/uploads/logo-sena-fondo-naranja-300x300.jpg",
    title: "Basico salud ocupacional",
    description: "",
    hours: "",
    year: "",
  },
  {
    provider: "SENA",
    url: "#",
    url_image: "https://lostramites.com.co/wp-content/uploads/logo-sena-fondo-naranja-300x300.jpg",
    title: "ABC para la constitucion de empresas",
    description: "",
    hours: "",
    year: "",
  },
  {
    provider: "SENA",
    url: "#",
    url_image: "https://lostramites.com.co/wp-content/uploads/logo-sena-fondo-naranja-300x300.jpg",
    title: "Creacion de bases de datos Access",
    description: "",
    hours: "",
    year: "",
  },
  {
    provider: "SENA",
    url: "#",
    url_image: "https://lostramites.com.co/wp-content/uploads/logo-sena-fondo-naranja-300x300.jpg",
    title: "English Dot Works Beginner",
    description: "",
    hours: "",
    year: "",
  },
])
export default {
  setup() {
    return {
      experience,
      shortCourses
    }
  },
  computed: {
    isMobile() {
      return this.$vuetify.display.xs || this.$vuetify.display.sm
    }
  }
}
</script>
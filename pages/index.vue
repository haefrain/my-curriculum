<template>
    <div>
        <v-row>
            <v-col cols="12" class="text-justify">
                Hola, soy un desarrollador web con más de 8 años de experiencia en programación en lenguajes backend y frontend, así como en consultas de base de datos con SQL. 
                He trabajado con diversos frameworks como Laravel, Symfony, Rails, Express, Vuejs, jQuery y React, adaptándome a las necesidades de cada proyecto.
            </v-col>
        </v-row>
        <v-row>
            <v-col cols="12" xs="12" sm="12" md="3" lg="3" xl="3">
                <v-img
                    aspect-ratio="1/1"
                    cover
                    src="efrain_hernandez.png"
                    ></v-img>
            </v-col>
            <v-col cols="12" xs="12" sm="12" md="9" lg="9" xl="9" class="text-justify">
                Tengo conocimiento de GIT y de la metodología ágil scrum, lo que me permite trabajar en equipo de forma eficiente y organizada.
                Me apasiona el desarrollo de software y soy autodidacta y curioso por nuevas tecnologías, especialmente las relacionadas con la inteligencia artificial.
                Busco siempre la optimización de procesos tanto para los clientes como para el desarrollo, ofreciendo soluciones creativas y de calidad.
            </v-col>
        </v-row>

        <v-row>
            <v-col cols="12">
                <v-chip-group>
                    <v-chip v-for="tech in listTech">{{tech}}</v-chip>
                </v-chip-group>
                
            </v-col>
        </v-row>

    </div>
</template>
<script>
const listImages = ref([
    "https://laravel.com/img/logotype.min.svg",
    "https://symfony.com/logos/symfony_black_02.png",
    "https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/Ruby_On_Rails_Logo.svg/1200px-Ruby_On_Rails_Logo.svg.png",
    "https://cdn.icon-icons.com/icons2/2699/PNG/512/expressjs_logo_icon_169185.png",
    "https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/2367px-Vue.js_Logo_2.svg.png",
    "https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/JQuery-Logo.svg/2560px-JQuery-Logo.svg.png",
    "https://download.logo.wine/logo/React_(web_framework)/React_(web_framework)-Logo.wine.png",
    "https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png",
    "https://cdn.worldvectorlogo.com/logos/scrumorg-1.svg",
    "https://logos-world.net/wp-content/uploads/2021/02/Jira-Emblem.png",
    "https://cdn-icons-png.flaticon.com/512/5968/5968313.png",
    "https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Postgresql_elephant.svg/993px-Postgresql_elephant.svg.png",
    "https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/MongoDB_Logo.svg/2560px-MongoDB_Logo.svg.png",
    "https://1000marcas.net/wp-content/uploads/2021/06/Redis-Logo.png",
    "https://cdn.freebiesupply.com/logos/large/2x/rethinkdb-logo-svg-vector.svg"
]);

const listTech = ref([
    "Laravel",
    "Symfony",
    "Rails",
    "Express",
    "Vuejs",
    "jQuery",
    "React",
    "Git",
    "Scrum",
    "Jira",
    "PostgreSQL",
    "MongoDB",
    "Redis",
    "RethinkDB",
].sort(() => Math.random() - 0.5))

export default {
    setup() {
        return {
            listImages,
            listTech
        }
    },
    head() {
        return {
            title: 'Resumen de Efrain Hernandez',
            meta: [
                {
                hid: 'description',
                name: 'description',
                content: 'Este es el resumen de mi CV en español como desarrollador fullstack web'
                },
                {
                hid: "og:title",
                property: "og:title",
                content: "Resumen de Efrain Hernandez",
                },
                {
                hid: "og:description",
                property: "og:description",
                content: "Este es el resumen de mi CV en español como desarrollador fullstack web",
                },
                {
                hid: "og:image",
                property: "og:image",
                content: "./efrain_hernandez.png",
                },
            ],
        }
    }
}
</script>
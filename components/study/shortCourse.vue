<template>
  <div>
    <v-row v-if="shortCourses && shortCourses.length > 0">
      <v-col cols="12">
        <h3>Cursos Cortos</h3>
        </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" xs="12" sm="12" md="6" lg="6" xl="6" xxl="6" v-for="item in shortCourses">
        <a :href="item.url" target="_blank" class="text-decoration-none">
          <v-card>
            <v-card-item>
              <v-card-title>
                <v-avatar :image="item.url_image" v-if="item.url_image"></v-avatar>
                {{ item.title }}
              </v-card-title>

              <v-card-subtitle>
                <div v-if="item.provider">
                  {{ item.provider }}
                </div>
                <div v-if="item.year">
                  {{ item.year }}
                </div>
                <div v-if="item.hours">
                  {{ item.hours }}
                </div>
              </v-card-subtitle>
            </v-card-item>

            <v-card-text v-if="item.description">
              {{item.description}}
            </v-card-text>
          </v-card>
        </a>
      </v-col>
    </v-row>
  </div>
</template>
<script setup>
const props = defineProps(['shortCourses']);
const shortCourses = ref(props.shortCourses);
</script>
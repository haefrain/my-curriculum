<template>
  <div>
    <v-row>
      <v-col cols="12">
        <v-timeline side="end" align="start">
              <v-timeline-item v-for="item in experience">
                <template v-slot:icon>
                  <v-avatar :image="item.url" cover></v-avatar>
                </template>
                <template v-slot:opposite>
                  <small>{{item.years}}</small>
                  <br />
                  <b>{{ item.title }}</b>
                </template>
                <div>
                  <div class="text-h6">{{item.position}}</div>
                  <p class="text-justify">
                    {{ item.description }}
                  </p>
                  <v-row v-if="item.tags">
                    <v-col cols="12">
                      <v-chip-group>
                        <v-chip v-for="tag in item.tags">{{tag}}</v-chip>
                      </v-chip-group>
                    </v-col>
                  </v-row>
                </div>
              </v-timeline-item>  
            </v-timeline>
      </v-col>
    </v-row>
  </div>
</template>
<script setup>
const props = defineProps(['experience']);
const experience = ref(props.experience);
</script>
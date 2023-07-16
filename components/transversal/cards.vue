<template>
  <div>
    <v-row>
      <v-col cols="12">
        <v-card v-for="item in experience" class="text-justify mb-3">
          <v-card-item>            
            <v-card-title>
              <v-avatar :image="item.url"></v-avatar>
              {{item.title}} 
            </v-card-title>
            <v-card-subtitle>
              {{item.position}} <br />
              <small>{{item.years}}</small>
            </v-card-subtitle>
          </v-card-item>

          <v-card-text>
            <v-row>
              <v-cols cols="12" class="ml-2 mr-2">
                {{ item.description }}
              </v-cols>
            </v-row>

            <v-row v-if="item.tags">
              <v-col cols="12">
                <v-chip-group>
                  <v-chip v-for="tag in item.tags">{{tag}}</v-chip>
                </v-chip-group>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<script setup>
const props = defineProps(['experience'])
const experience = ref(props.experience)
</script>
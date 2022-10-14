<template>
  <section id="recent">
    <v-container class="text-center">
      <h2 class="section-title large">Галерея последних работ</h2>
      <p>Выберите понравившеюся из готовых композиций или создайте свою собственную</p>
    </v-container>
    <v-row no-gutters>
      <v-col v-for="(image, n) in IMAGES" :key="`recentImage${n}`" cols="12" sm="6" md="3">
        <pre-image :src="image" aspect-ratio="1.5" />
      </v-col>
    </v-row>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "@nuxtjs/composition-api"

const IMAGES = [`recent/1.jpg`, `recent/2.jpg`, `recent/3.jpg`, `recent/4.jpg`]

export default defineComponent({
  setup() {
    return {
      IMAGES,
    }
  },
})
</script>

<style lang="sass" scoped>
#recent
  background-color: black
  color: white
</style>

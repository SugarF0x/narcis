<template>
  <section id="quote" class="text-center">
    <v-icon color="white" size="80">mdi-flower</v-icon>
    <p class="text text-justify text-sm-center">
      "Тем, что я стал художником, я обязан цветам"
    </p>
    <h4 class="author">- Клод Моне</h4>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "@nuxtjs/composition-api"

export default defineComponent({
  setup() {},
})
</script>

<style lang="sass" scoped>
#quote
  background: linear-gradient(0deg, rgba(0,0,0,0.65), rgba(0,0,0,0.65)), url("~assets/img/worker_bg.webp") no-repeat center
  background-size: cover
  padding: 48px
  color: white

  @media(min-width: 960px)
    padding: 96px
  @media(min-width: 1264px)
    padding: 96px 192px
  @media(min-width: 1904px)
    padding: 96px 384px

.text
  font-style: italic

.author
  font-family: "Courier New", monospace
  margin-top: 16px
  font-size: 1.2em
</style>

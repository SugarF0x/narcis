<template>
  <section id="record">
    <v-container>
      <v-row justify="center" align="center">
        <v-col cols="12" md="5" lg="4">
          <h4 class="display-1 s-text--primary font-weight-bold text-center">
            <a href="tel:+79160000000">+7 (916) 000 00 00</a>
          </h4>
          <h4 class="display-1 s-text--primary font-weight-bold text-center">
            <a href="mailto:info@narcis.com">info@narcis.com</a>
          </h4>
        </v-col>
        <v-col cols="12" md="5" lg="4" class="text-center">
          <h3>Следите за нами в телеграмм!</h3>
          <p>
            <i>
              @narcisFlowers
            </i>
          </p>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "@nuxtjs/composition-api"

export default defineComponent({
  setup() {},
})
</script>

<style lang="sass" scoped>
#record
  color: white
  background-color: black

  a
    text-decoration: none
    color: unset

.card-title
  word-break: normal
</style>

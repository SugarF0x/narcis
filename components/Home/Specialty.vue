<template>
  <section id="specialty" class="s-bg--primary-dark">
    <div class="bg">
      <v-container class="text-center container">
        <h2 class="section-title large">Букеты</h2>
        <v-row no-gutters justify="center" class="mx-sm-8 mx-md-16">
          <v-col v-for="(col, colIndex) in cards" :key="`card-col-${colIndex}`" cols="12" sm="6" class="px-xl-16">
            <Card color="primary-dark" class="transparent text--white">
              <template #title>
                <div class="display-2 mb-2 ass">
                  {{ col.icon }}
                </div>
                {{ col.title }}
              </template>
              <template #text>
                <p>
                  {{ col.text }}
                </p>
              </template>
            </Card>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "@nuxtjs/composition-api"

export default defineComponent({
  setup() {
    return {
      cards: cards.map((a) => new CardData(...a)),
    }
  },
})

const cards: [string, string, string][] = [
  ["S", "15 000₽ - 20 000₽", "Комплимент для любимых"],
  ["M", "20 000₽ - 50 000₽", "Для значимых моментов"],
  ["L", "50 000₽ - 100 000₽", "Для головокружительного эффекта"],
  ["Premium", "100 000₽+", "Для незабываемых событий"],
]

class CardData {
  icon: string
  title: string
  text: string

  constructor(icon: string, title: string, text: string) {
    this.icon = icon
    this.title = title
    this.text = text
  }
}
</script>

<style lang="sass" scoped>
#specialty
  position: relative
  display: flex

.bg
  width: 100% //noinspection CssUnknownTarget
  background: linear-gradient(0deg, rgba(26,26,26,0.9), rgba(26,26,26,0.9)), url("~assets/img/city_bg.png") no-repeat center
  background-size: cover

.container
  max-width: 1100px

.ass
  color: #FFCE3E
</style>

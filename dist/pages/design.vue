<template>
  <v-container fluid class="">
    <v-row align="center" justify="center">
      <div class="d-flex">
        <div data-aos="flip-left" data-aos-delay="500">
          <v-hover v-slot="{ hover }">
            <div
              :class="hover ? 'text-decoration-underline primary--text' : ''"
              style="cursor: pointer; font-size: 17px"
              class="px-4 btn"
              @click="scrollGraphic()"
            >
              Graphic Design
            </div>
          </v-hover>
        </div>
        <div class="px-3 grey--text">●</div>

        <div>
          <v-hover v-slot="{ hover }">
            <div
              :class="hover ? 'text-decoration-underline primary--text' : ''"
              style="cursor: pointer; font-size: 17px"
              class="px-4 btn"
              @click="scrollAchievement()"
            >
              Achievement
            </div>
          </v-hover>
        </div>
        <div class="px-3 grey--text">●</div>

        <div>
          <v-hover v-slot="{ hover }">
            <div
              :class="hover ? 'text-decoration-underline primary--text' : ''"
              style="cursor: pointer; font-size: 17px"
              class="px-4 btn"
              @click="scrollLoffee()"
            >
              Loffee
            </div>
          </v-hover>
        </div>

        <div class="px-3 grey--text">●</div>

        <div>
          <v-hover v-slot="{ hover }">
            <div
              :class="hover ? 'text-decoration-underline primary--text' : ''"
              style="cursor: pointer; font-size: 17px"
              class="px-4 btn"
              @click="scrollPromofy()"
            >
              Promofy
            </div>
          </v-hover>
        </div>
        <div class="px-3 grey--text">●</div>

        <div data-aos="flip-left" data-aos-delay="500">
          <v-hover v-slot="{ hover }">
            <div
              :class="hover ? 'text-decoration-underline primary--text' : ''"
              style="cursor: pointer; font-size: 17px"
              class="px-4 btn"
              @click="scrollForFun()"
            >
              Just For Fun
            </div>
          </v-hover>
        </div>
      </div>
    </v-row>
    <GraphicDesign />
    <v-row class="pt-16">
      <Achievement />
    </v-row>
    <v-row class="pt-16">
      <Loffee />
    </v-row>
    <v-row class="pt-16">
      <Promofy />
    </v-row>
    <v-row class="pt-16">
      <Web />
    </v-row>
    <v-row class="pt-16">
      <ForFun />
    </v-row>
    <ScrollUp />
  </v-container>
</template>

<script>
import GraphicDesign from '../components/design/graphic.vue'
import Loffee from '../components/design/loffee.vue'
import Promofy from '../components/design/promofy.vue'
import ForFun from '../components/design/fun.vue'
import Achievement from '../components/design/achievement.vue'
import ScrollUp from '../components/ScrollUp.vue'
import Web from '../components/design/web.vue'
export default {
  components: {
    GraphicDesign,
    Loffee,
    Promofy,
    ForFun,
    Achievement,
    ScrollUp,
    Web,
  },
  data: () => ({
    icons: [
      { name: 'mdi-facebook', url: 'https://web.facebook.com/momol3ng/' },
      { name: 'mdi-instagram', url: 'https://www.instagram.com/_momoleng_/' },
      {
        name: 'mdi-linkedin',
        url: 'https://www.linkedin.com/in/mouyleng-heng-b549b81a9/',
      },
      { name: 'mdi-twitter', url: 'https://twitter.com/Momol3ng' },
    ],
  }),
  methods: {
    socialMedia(icon) {
      window.open(icon.url)
    },
    scrollGraphic() {
      const graphicid = document.getElementById('graphic')
      graphicid.scrollIntoView({ behavior: 'smooth' })
    },
    scrollAchievement() {
      const achievementid = document.getElementById('achievement')
      achievementid.scrollIntoView({ behavior: 'smooth' })
    },
    scrollLoffee() {
      const loffeeid = document.getElementById('loffee')
      loffeeid.scrollIntoView({ behavior: 'smooth' })
    },
    scrollPromofy() {
      const promofyid = document.getElementById('promofy')
      promofyid.scrollIntoView({ behavior: 'smooth' })
    },
    scrollWeb() {
      const webid = document.getElementById('web')
      webid.scrollIntoView({ behavior: 'smooth' })
    },
    scrollForFun() {
      const forfunid = document.getElementById('forfun')
      forfunid.scrollIntoView({ behavior: 'smooth' })
    },
  },
}
</script>

<style lang="scss" scoped>
// @import './styles/_variables.scss';
</style>
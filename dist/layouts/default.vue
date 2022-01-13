<template>
  <v-app light>
    <div class="pt-8 pr-8 hidden-sm-and-down">
      <SocialMedia size="25px" />
    </div>
    <v-container fluid class="py-6" hidden-sm-and-down>
      <div class="text-center d-flex align-center justify-center">
        <div class="d-flex" v-for="item in items" :key="item">
          <v-hover v-slot="{ hover }">
            <div
              :class="hover ? ' primary--text' : ''"
              style="
                cursor: pointer;
                font-size: 17px;
                font-family: 'Open Sans', sans-serif;
              "
              class="px-4 text-uppercase font-weight-regular subtitle-2"
              @click="onClick(item)"
            >
              {{ item.title }}
            </div>
          </v-hover>
          <div
            class="px-2 font-weight-black primary--text"
            v-if="item.title == 'Habits' ? false : true"
          >
            |
          </div>
        </div>
      </div>
    </v-container>

    <v-container fluid class="pt-16" hidden-md-and-up>
      <div class="pt-1 d-flex justify-center">
        <div v-for="item in items" :key="item.title" class="px-1">
          <div class="d-flex">
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-hover v-slot="{ hover }">
                  <div
                    style="cursor: pointer; font-size: 17px"
                    class="px-2"
                    @click="onClick(item)"
                    v-bind="attrs"
                    v-on="on"
                  >
                    <v-icon
                      @click="onClick(item)"
                      :class="hover ? ' primary--text' : ''"
                      size="26px"
                      >{{ item.icon }}</v-icon
                    >
                  </div>
                </v-hover>
              </template>
              <span>{{ item.title }}</span>
            </v-tooltip>
            <div
              class="px-2 font-weight-black primary--text"
              v-if="item.title == 'Resume' ? false : true"
            >
              |
            </div>
          </div>
        </div>
      </div>
    </v-container>

    <v-main class="ma-5">
      <v-container fluid class="px-16">
        <nuxt />
      </v-container>
    </v-main>

    <!-- <v-divider></v-divider>
    <v-card-text class="text-center grey--text text--darken-2 py-2 px-8"
      ><span class="font-weight-bold">Copyright</span> ©
      <span class="font-weight-bold">Mouyleng Heng</span>
      <span>✿ Know Me More ✿</span>
      <SocialMedia size="25px" />
    </v-card-text> -->
  </v-app>
</template>

<script>
import SocialMedia from '~/components/social_media.vue'
export default {
  components: { SocialMedia },
  data() {
    return {
      items: [
        { title: 'About', url: '/about', icon: 'mdi-face-woman-shimmer' },
        {
          title: 'Works',
          url: '/works',
          icon: 'mdi-monitor-dashboard',
        },
        { title: 'Design', url: '/design', icon: 'mdi-pencil-ruler' },
        { title: 'Resume', url: '/resume', icon: 'mdi-file-account' },
        // { title: 'Skillset', url: '/skills', icon: 'mdi-xml' },
        // { title: 'Life', url: '/la_vie', icon: 'mdi-sail-boat' },
        // { title: 'Habits', url: '/habits', icon: 'mdi-palette-outline' },
      ],
    }
  },
  methods: {
    onClick(item) {
      this.$router.push(item.url)
    },
  },
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');
</style>

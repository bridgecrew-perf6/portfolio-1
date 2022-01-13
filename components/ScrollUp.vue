<template>
  <div id="scrollup">
    <v-btn
      v-show="fab"
      v-scroll="onScroll"
      small
      color="primary lighten-1"
      class="font-weight-regular subtitle-2"
      style="background-color: white"
      fixed
      outlined
      bottom
      right
      @click="toTop"
    >
      <v-icon size="16" class="pr-1">mdi-arrow-up-circle</v-icon>
      <span>Back to top</span>
    </v-btn>
  </div>
</template>

<script>
export default {
  name: 'ScrollUp',
  components: {},
  data() {
    return {
      overlay: false,
      hover: false,
      fab: false,
    }
  },
  methods: {
    onScroll(e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.fab = top > 20
    },
    toTop() {
      this.$vuetify.goTo(0)
    },
  },
}
</script>

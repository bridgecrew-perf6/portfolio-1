<template>
  <div class="pt-1 d-flex justify-end">
    <div class="px-1">
      <v-btn to="/" icon>
        <v-icon class="grey--text" :size="size">mdi-home</v-icon>
      </v-btn>
    </div>
    <div v-for="icon in icons" :key="icon" class="px-1">
      <v-btn icon target="_blank">
        <v-icon @click="socialMedia(icon)" class="grey--text" :size="size">{{
          icon.name
        }}</v-icon>
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    size: { type: String },
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
      { name: 'mdi-wordpress', url: 'https://mouyleng67720287.wordpress.com' },
    ],
  }),
  methods: {
    socialMedia(icon) {
      window.open(icon.url)
    },
  },
}
</script>

<style lang="scss" scoped>
</style>
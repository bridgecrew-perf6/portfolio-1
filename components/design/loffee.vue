<template>
  <v-container fluid class="pt-16">
    <v-row align="center" justify="center">
      <div
        id="loffee"
        class="text-center font-weight-medium py-5"
        style="font-size: 30px"
      >
        <v-avatar>
          <img
            style="border: 1px solid #e6e6e6"
            src="~/assets/logo/loffee.JPG"
          />
        </v-avatar>
        Loffee Mobile Prototype
        <v-icon size="30">mdi-cellphone-text mdi-rotate-135</v-icon>
      </div>
    </v-row>
    <v-row>
      <v-col
        v-for="img in image"
        :key="img"
        class="d-flex child-flex"
        cols="12"
        sm="4"
        md="3"
        lg="2"
        xl="2"
      >
        <v-img
          :src="`${img.img}`"
          @click="showDetails(img)"
          class="grey lighten-2"
        >
          <template v-slot:placeholder>
            <v-row class="fill-height ma-0" align="center" justify="center">
              <v-progress-circular
                indeterminate
                color="grey lighten-5"
              ></v-progress-circular>
            </v-row>
          </template>
        </v-img>
      </v-col>
      <v-dialog v-model="dialog" max-width="70%">
        <v-card tile outlined>
          <!-- <v-card-title class="px-11 pt-8">
            <div style="font-size: 22px; color: #627080">
              Title
              <div style="font-size: 14px" class="py-0 font-weight-regular">
                Subtitle
              </div>
            </div>
          </v-card-title> -->
          <v-card-text class="pt-3 px-7">
            <v-container>
              <v-row>
                <v-col>
                  <v-img :src="`${picture.img}`" class="grey lighten-2"></v-img>
                </v-col>
                <!-- <v-col cols="6"><div>card</div></v-col> -->
              </v-row>
            </v-container>
          </v-card-text>
        </v-card>
        <!-- <v-img
            :src="`${n.img}`"
            aspect-ratio="1"
            class="grey lighten-2"
          ></v-img> -->
      </v-dialog>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    dialog: false,
    picture: '',
    image: [
      { img: require('@/assets/prototype/loffee/1.png') },
      { img: require('@/assets/prototype/loffee/2.png') },
      { img: require('@/assets/prototype/loffee/3.png') },
      { img: require('@/assets/prototype/loffee/4.png') },
      { img: require('@/assets/prototype/loffee/5.png') },
      { img: require('@/assets/prototype/loffee/6.png') },
      { img: require('@/assets/prototype/loffee/7.png') },
      { img: require('@/assets/prototype/loffee/8.png') },
      { img: require('@/assets/prototype/loffee/9.png') },
      { img: require('@/assets/prototype/loffee/10.png') },
      { img: require('@/assets/prototype/loffee/11.png') },
    ],
  }),
  methods: {
    showDetails(img) {
      this.dialog = true
      console.log('image', img)
      this.picture = img
    },
  },
}
</script>

<style lang="scss" scoped>
</style>
<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <div
        id="forfun"
        class="text-center font-weight-medium py-5"
        style="font-size: 30px"
      >
        <v-icon size="30">mdi-pencil-ruler mdi-rotate-45</v-icon>

        Just For Fun <span></span>
      </div>
    </v-row>
    <v-row>
      <v-col
        v-for="img in image"
        :key="img"
        class="d-flex child-flex"
        cols="6"
        sm="4"
        md="3"
        lg="3"
        xl="3"
      >
        <v-img
          :src="`${img.img}`"
          aspect-ratio="1"
          class="grey lighten-2"
          @click="showDetails(img)"
          style="border: 1px solid #e6e6e6"
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
                  <v-img
                    :src="`${picture.img}`"
                    style="border: 1px solid #e6e6e6"
                    class="grey lighten-2"
                  ></v-img>
                </v-col>
              </v-row>
            </v-container>
          </v-card-text>
        </v-card>
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
      { img: require('@/assets/drawing/1.png') },
      { img: require('@/assets/drawing/2.png') },
      { img: require('@/assets/drawing/3.png') },
      { img: require('@/assets/drawing/4.png') },
      { img: require('@/assets/drawing/5.png') },
      { img: require('@/assets/drawing/6.png') },
      { img: require('@/assets/drawing/7.png') },
      { img: require('@/assets/drawing/8.png') },
      { img: require('@/assets/drawing/9.png') },
      { img: require('@/assets/drawing/10.png') },
      { img: require('@/assets/drawing/11.png') },
      { img: require('@/assets/drawing/12.png') },
    ],
  }),
  methods: {
    showDetails(img) {
      this.dialog = true
      this.picture = img
    },
  },
}
</script>

<style lang="scss" scoped>
</style>
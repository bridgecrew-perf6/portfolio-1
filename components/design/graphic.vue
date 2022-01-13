<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <div
        id="graphic"
        class="text-center font-weight-medium py-5"
        style="font-size: 30px"
      >
        <v-icon size="30">mdi-pencil-ruler mdi-rotate-45</v-icon>

        Graphic Design <span></span>
      </div>
    </v-row>
    <v-row>
      <v-col
        v-for="img in image"
        :key="img.index"
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
                    class="grey lighten-2"
                    style="border: 1px solid #e6e6e6"
                  ></v-img>
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
    picture: '',
    dialog: false,
    image: [
      { img: require('@/assets/graphic/1.png') },
      { img: require('@/assets/graphic/2.png') },
      // { img: require('@/assets/graphic/3.png') },
      { img: require('@/assets/graphic/4.png') },
      { img: require('@/assets/graphic/5.png') },
      { img: require('@/assets/graphic/6.png') },
      { img: require('@/assets/graphic/7.png') },
      { img: require('@/assets/graphic/8.png') },
      { img: require('@/assets/graphic/9.png') },
      { img: require('@/assets/graphic/10.png') },
      { img: require('@/assets/graphic/11.png') },
      { img: require('@/assets/graphic/12.png') },
      { img: require('@/assets/graphic/13.png') },
      { img: require('@/assets/graphic/14.png') },
      { img: require('@/assets/graphic/15.png') },
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
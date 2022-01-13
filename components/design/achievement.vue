<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <div
        id="achievement"
        class="text-center font-weight-medium py-5"
        style="font-size: 30px"
      >
        <v-icon size="30">mdi-pencil-ruler mdi-rotate-45</v-icon>
        Achievement
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
    picture: '',
    dialog: false,
    image: [{ img: require('@/assets/achievement/3.png') }],
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
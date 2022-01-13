<template>
  <v-row justify="center" align="center" class="pt-16">
    <v-col cols="1">
      <div class="vertic_text">
        <p
          class="
            subText1
            grey--text
            text--lighten-1
            display-2
            font-weight-medium
          "
        >
          Welcome To My Portfolio
        </p>
      </div>
    </v-col>
    <v-col cols="10">
      <UserFriendly />
    </v-col>
    <v-col cols="1">
      <div class="vertic_text d-flex text-center justify-center align-center">
        <p
          class="
            subText
            grey--text
            text--lighten-1
            display-1
            font-weight-medium
          "
        >
          About Me
        </p>
        <div class="text-center px-4">
          <v-btn icon to="/about">
            <v-icon class="grey--text text--lighten-1" size="30"
              >mdi-chevron-double-right</v-icon
            ></v-btn
          >
        </div>
      </div>
    </v-col>
  </v-row>
</template>

<script>
import UserFriendly from '~/components/user_friendly.vue'
export default {
  components: {
    UserFriendly,
  },
}
</script>

<style>
.vertic_text {
  /* background-color: hsla(33, 95%, 69%, 1); */
  height: auto;
}
.subText {
  transform: rotate(360deg);
  writing-mode: vertical-lr;
  padding-bottom: 1rem;
}
.subText1 {
  transform: rotate(180deg);
  writing-mode: vertical-lr;
  padding-bottom: 1rem;
}
</style>

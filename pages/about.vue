<template>
  <v-container fluid class="px-0">
    <v-row align="start" justify="center">
      <div class="text-center">
        <v-img>
          <img
            src="~/assets/profile-1.jpg"
            class="rounded-circle pa-1"
            width="200px"
            style="border: 1px solid #e6e6e6"
          />
        </v-img>
      </div>
    </v-row>
    <v-row align="start" justify="center" class="pt-7">
      <div class="text-center introduction font-weight-bold">
        Hi, I'm Mouyleng, nice to meet you!
      </div>
    </v-row>

    <v-row align="start" justify="center" class="pt-6 px-10">
      <v-card
        elevation="0"
        :style="
          this.$vuetify.breakpoint.mdAndUp
            ? 'width: 55%; margin: 0 auto'
            : 'width: 100%; margin: 0 auto'
        "
      >
        <p class="py-1" style="font-family: 'Open Sans', sans-serif">
          I am currently in my senior year majoring in Software Engineering in
          Kirirom Institute of Technology - KIT. I am passionate about UI/UX
          design and Frontend Web Developement. I have been working with these
          field for the past two years now. Coding is suck sometimes. So I have
          somethings else to occupy myself like design or doing somethings
          creative. Always accept new challenges. Willing to learn new things
          and discover coding skills. Believe in Hardwork and Teamwork. Every
          succeess is not coincidental but it comes from working hard,
          commitment, learning and sacrifice. Hardwork pays off.
        </p>
      </v-card>
    </v-row>

    <v-row align="start" justify="center" class="pt-10">
      <v-col>
        <div class="text-center py-6">
          <!-- <v-img>
            <img
              src="~/assets/profile-1.jpg"
              class="rounded-lg pa-1"
              width="300px"
              style="border: 1px solid #e6e6e6"
            />
          </v-img> -->

          <!-- <div class="pt-5 px-16">
            <div class="font-italic px-14" style="font-size: 18px">
              <span class="text-h5">"</span>
              However <b>tiresome</b> it becomes, never let yourself succumb to
              <b>despair</b>. <span class="text-h5">"</span>
            </div>
          </div> -->
        </div>
      </v-col>
      <!-- <v-col>
        <div class="py-4">
          <div class="py-2 font-weight-bold primary--text text-h5">
            Who Am I?
          </div>

          <div class="py-1">
            Hello, My name is Heng Mouyleng. I am currently in my senior year
            majoring in Software Engineering in Kirirom Institute of Technology
            - KIT. I am an UI/UX designer and Frontend developer.
          </div>
        </div>
      </v-col> -->
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({}),
  methods: {},
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');

div.introduction {
  font-family: 'Open Sans', sans-serif;
  font-size: 20px;
}
</style>
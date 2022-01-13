<template>
  <v-container fluid class="px-10">
    <v-row
      align="center"
      class="pt-10 px-2"
      justify="center"
      v-for="item in items"
      :key="item.title"
    >
      <v-col cols="12" md="6" lg="6" xl="6">
        <div style="font-size: 25px" class="text-center">
          <span class="text-h5">"</span> {{ item.title }}
          <span class="text-h5">"</span>
        </div>
        <div class="text-center subtitle-2 font-weight-regular font-italic">
          {{ item.time }}
        </div>
      </v-col>
      <v-col cols="12" md="6" lg="6" xl="6">
        <div style="border-left: 1px solid grey; font-size: 18px" class="pl-5">
          ☉ {{ item.description }}
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        title: 'Digital Marketing',
        time: 'July - December 2021',
        description:
          '6 months experience with Digital Marketing, Creating content and script of videos.',
      },
      {
        title: 'Graphic Design',
        time: 'July - December 2021',
        description:
          'Photo and video shooting, Design posters and Edit short video. Outsource graphic designing for a kid international school, and some internal school event.',
      },
      {
        title: 'UI/UX Design',
        time: 'July - August 2020',
        description:
          'Prototyping a mobile application “Promofy” for project to join a Competition',
      },
      {
        title: 'Frontend Developing',
        time: 'December 2020 - Now',
        description:
          'One year experience with Vuejs as well as Nuxtjs, and Vueitfy. Developing the internal system from scratch with full of functionalities logics and dashboards.',
      },
    ],
  }),
}
</script>

<style >
::-webkit-scrollbar {
  display: none;
}
</style>
<template>
  <div class="primary--text text-darken-2">
    <v-row
      align="center"
      justify="center"
      class="px-auto font-weight-light"
      style="font-size: 3vw"
    >
      <div class="py-2 kh font-weight-bold">{{ khmer }}</div>
    </v-row>
    <v-row
      align="center"
      justify="center"
      class="px-auto font-weight-light"
      style="font-size: 3vw"
    >
      <div class="py-2 eng font-weight-bold">{{ english }}</div>
    </v-row>
    <v-row
      align="center"
      justify="center"
      class="px-auto font-weight-light"
      style="font-size: 3vw"
    >
      <div class="py-2 fr font-weight-bold">{{ french }}</div>
    </v-row>
    <v-row
      align="center"
      justify="center"
      class="px-auto font-weight-light"
      style="font-size: 3vw"
    >
      <div class="py-2 jp">{{ japanese }}</div>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    khmer: '',
    english: '',
    french: '',
    japanese: '',
  }),
  mounted() {
    const time = new Date().getHours()
    if (time < 12) {
      this.khmer = 'អរុណ​សួស្តី'
      this.english = 'Good Morning'
      this.french = 'Bon Matin'
      this.japanese = 'おはようございます。'
    } else if (time >= 12 && time < 17) {
      this.khmer = 'សាយណ្ណសួស្តី'
      this.english = 'Good Afternoon'
      this.french = 'Bonne Après-Midi'
      this.japanese = 'こんにちは'
    } else {
      this.khmer = 'រាត្រី​សួស្តី'
      this.english = 'Good Evening'
      this.french = 'Bonne Nuit'
      this.japanese = 'こんばんは'
    }
  },
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Dosis:wght@200&family=Koh+Santepheap:wght@100&family=Rampart+One&display=swap');
div.jp {
  font-family: 'Rampart One', cursive;
}
div.eng,
div.fr {
  font-family: 'Dosis', sans-serif;
}
div.kh {
  font-family: 'Koh Santepheap', cursive;
}
</style>
<template lang="html">
  <b-row class="informative-section">
    <b-col cols="12">
      <h2>{{ title }}</h2>
    </b-col>

    <b-col cols="4"
      v-for="(card, index) in cards"
      :key="index"
      class="info-card">
      <img :src="card.img" alt="">
      <h4 class="card-title">{{ card.cardTitle }}</h4>
      <p class="card-text">{{ card.cardText }}</p>
    </b-col>
  </b-row>
</template>

<script>
export default {
  data() {
    return {
      title: 'Modernize your cloud infrastructure—fast',
      cards: [
        {
          img: require('~/assets/timer.svg'),
          cardTitle: 'Ready to go in seconds',
          cardText: 'Save time with preconfigured environments that already have all the prerequisites installed – which removes the hassle of spinning up and provisioning servers.'
        },
        {
          img: require('~/assets/addTool.svg'),
          cardTitle: 'The tools you need – in one place',
          cardText: 'We review everyday apps and cutting-edge technologies so you always have access to the most efficient tools to build your business.'
        },
        {
          img: require('~/assets/documentIcon.svg'),
          cardTitle: 'Spend your time developing',
          cardText: 'Say goodbye to research, configuration, and manual setup – our 1-Click Apps handle it all for you.'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.informative-section {
  padding: 80px 0;

  h2 {
    font-weight: 700;
    text-align: center;
    margin-bottom: 50px;
  }

  .info-card img {
    margin-bottom: 20px;
  }
}
</style>

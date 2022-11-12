<template>
  <div id="value-section" class="value-wrapper">
    <h1>Our Values</h1>

    <div class="card-list">
      <Card class = "card" v-for="card in cards" :key="card.text" :card="card" />
    </div>
  </div>
</template>

<script>
import Card from './CardComponent.vue'

export default {
  components: {
    'Card': Card
  },
  data(){
    return {
      cards: [
        {
          text: 'Professional',
          image: 'value1.jpg'
        },
        {
          text: 'Teamwork',
          image: 'value2.jpg'
        },
        {
          text: 'Excelence',
          image: 'value3.jpg'
        },
        {
          text: 'Respect',
          image: 'value4.jpg'
        },
        {
          text: 'Integrity',
          image: 'value5.jpg'
        },
      ]
    }
  }
}
</script>

<style scoped>
.value-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  min-height: 100vh;

  padding: 6rem;
}

h1 {
  position: relative;
  color: white;
  font-size: 6rem;
  overflow: hidden;
  margin-bottom: 4rem;
}

h1::before {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  background-color: white;
  width: 100%;
  height: 10px;

  z-index: -1;
  transform: translateX(-101%);
  transition: all 0.2s ease;
}

h1:hover::before {
  transform: translateX(0);
}

.card-list {
  display: flex;
  width: 90vw;
  min-width: 600px;

  flex-basis: 300px;
  flex-grow: 1;
  overflow-x: scroll;
  overflow-y: hidden;

  justify-content: center;
}

.card {
  
  transition: all 0.5s ease;
}

.card:hover {
  transform: translateY(-2rem);
}

.card:hover ~.card {
  transform: translateX(150px);
}

.card:not(:first-child){
  margin-left: -150px;
}
</style>
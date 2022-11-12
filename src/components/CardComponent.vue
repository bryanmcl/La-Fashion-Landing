<template>
  <div class="container">
    <img :src= "require(`../assets/images/${card.image}`)" alt="img">
    <h1 class="title">{{card.text}}</h1>
    <div class="box-effect"></div>
  </div>
</template>

<script>

export default {
  props:['card'],
  data() {
    return {
    }
  },
}
</script>

<style scoped>
.container {
  display: flex;

  position: relative;
  min-width: 300px;
  width: 20vw;
  height: 400px;
  margin: 2rem 0;

  background: #222;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: -1rem 1rem 2rem #111;
}

img {
  position: absolute;
  top: 0;
  left: 0;
  object-fit: cover;

  width: 100%;
  height: 100%;
  transition: all 0.5s ease;
}

.title {
  position: relative;
  height: 2.5rem;

  margin-left: 1rem;
  margin-top: 1rem;
  color: white;
  font-size: 2rem;
  font-weight: bold;
  z-index: 1;

  transform: translateY(-150%);
  
  transition: all 0.5s ease;
}

.title::before {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  background-color: white;
  width: 100%;
  height: 5px;

  z-index: -1;
  transform: translateX(-120%);
  transition: all 0.2s ease;
}

.title:hover::before {
  transform: translateX(0);
}

.container:hover .title {
  transform: translateY(0);
}

.container:hover img {
  transform: scale(1.2) rotateZ(10deg);
  filter: grayscale(100%) brightness(0.6);
}

.box-effect {
  position: absolute;
  width: 100%;
  height: 100%;

  /* box-shadow: 2rem 0 3rem #000; */
  /* background: linear-gradient(to top,  rgba(0, 0, 0, 0.519), rgba(0,0,0,0)); */
}

</style>
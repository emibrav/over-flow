<template>
  <div class="tech-container">
    <div>
      <p class="text">TRUSTED BY THOUSANDS OF ORGANIZATIONS ACROSS THE GLOBE</p>
    </div>
    <transition name="appear">
      <div class="icons">
        <img src="../assets/amazon.svg" alt="">
        <img src="../assets/netflix.svg" alt="">
        <img src="../assets/spotify.svg" alt="">
        <img src="../assets/microsoft.svg" alt="">
        <img src="../assets/facebook.svg" alt="">
        <img src="../assets/disney.svg" alt="">
        <img src="../assets/yahoo.svg" alt="">
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  name: "TechsBar"
}
</script>
<style scoped>
.tech-container {
  max-width: 100%;
  background-color: #d5f3ff;
  padding: 2rem 1rem;
}
.text {
  text-align: center;
  font-weight: bold;
  font-size: 0.7rem;
  letter-spacing: 2px;
  margin-bottom: 3rem;
}
.icons {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  padding: 2rem 4rem;
}
</style>
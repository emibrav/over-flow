/* eslint-disable prettier/prettier */
<template>
  <div class="container">
    <div class="text">
      <h2>Turn your designs into <br>
      beautiful user flows
      </h2>
      <p>Create beautiful user flow diagrams and design presentations in no time. Works with Adobe XD, Figma, Sketch, and Photoshop.</p>
      <button class="see-how-button">See how ></button>
    </div>
    <div class="image">
      <img src="../assets/turn-designs.png" alt="">
    </div>
  </div>
</template>
<script>
export default {
  name: "TurnDesigns"
}
</script>
<style scoped>
.container {
  /* border: 1px solid salmon; */
  max-width: 100%;
  margin: 4rem auto;
  padding-left: 2.2rem;
  /* display: flex; */
  /* justify-content: space-between; */
  /* align-items: center; */
  position: relative;
}
h2 {
  font-weight: bold;
  text-align: left;
  color: #161637;
  font-size: 2rem;
  padding-top: 2rem;
}
.see-how-button {
  color: #0085e4;
  background-color: white;
  margin-top: 1.5rem;
  /* width: 80px; */
  max-width: max-content;
  border: none;
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
}
.image {
  overflow: hidden;
  margin: 1rem;
  /* border: 2px solid #04161d; */
  background-color: #d5f3ff;
  position: absolute;
  top: 50%;
  left: 75%;
  transform: translate(-50%, -50%);
  height: 228px;
  width: 452px;
  border-radius: 344px 344px 0 0;
}
.text {
  /* border: 1px solid green; */
  max-width: 50%;
  line-break: loose;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}
img {
  width: 400px;
  height: 400px;
  margin: -2rem;
}
p {
  text-align: left;
  line-height: 1.7rem;
  margin-top: 1em; 
}
</style>
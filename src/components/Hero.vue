/* eslint-disable prettier/prettier */
<template>
  <div class="container">
    <div class="hero-left">
      <div class="title">
        <h1 class="text">
          Communicate <br />
          your designs like <br />
          never before
        </h1>
        <h4 class="text">
          Create interactive user flow diagramas that tell a story.
        </h4>
      </div>
      <div></div>
      <div class="buttons">
        <start-button text="start for free" class="start-button" />
        <start-button
          text="see examples"
          class="examples-button"
          bgColor="#fff"
        />
      </div>
      <div class="techs"></div>
    </div>
    <div class="hero-right">
      <div>
        <img alt="Laptop" src="../assets/pngegg.png" />
        <bottom-right class="bottom-right" />
        <top-left class="top-left" />
        <top-right class="top-right" />
        <play-button class="play-button" />
      </div>
    </div>
  </div>
</template>
<script>
import StartButton from "@/components/Buttons/StartButton.vue"
import BottomRight from "@/components/FloatingCards/BottomRight.vue"
import TopLeft from "./FloatingCards/TopLeft.vue"
import TopRight from "./FloatingCards/TopRight.vue"
import PlayButton from "@/components/Buttons/PlayButton.vue"

export default {
  name: "Hero",
  components: { StartButton, BottomRight, TopLeft, TopRight, PlayButton },
  methods: {
    scroll() {
      window.scroll({
        top: 300,
        left: 500,
        behavior: `"smooth",`
      })
    }
  }
}
</script>
<style scoped>
img {
  width: 450px;
  height: 450px;
}
.text {
  color: #161637;
}
.container {
  width: 70%;
  margin: 7rem auto 4rem auto;
  display: flex;
  justify-content: space-between;
}
h1 {
  font-size: 2.8rem;
  text-align: left;
}
h4 {
  text-align: left;
  font-weight: normal;
}
.hero-right {
  width: 50%;
  /* border: 1px solid salmon; */
  position: relative;
}
.hero-left {
  /* border: 1px solid salmon; */
  width: 50%;
  color: black;
  padding: 4.5rem 0;
  margin-right: 1rem;
}
.examples-button {
  border: 1px solid #2c2c96;
  color: #2c2c96;
  margin-left: 1.5rem;
  background: white;
  transition: 0.5s;
}
.examples-button:hover {
  box-shadow: inset 0 0 0 1px #3d3dc3;
  background-color: white;
}

.buttons {
  margin-top: 30px;
  display: flex;
}
.top-left {
  position: absolute;
  top: 8%;
  left: calc(3% - 50px);
  animation: 4s infinite alternate slideup-top;
}
.bottom-right {
  position: absolute;
  right: -15%;
  bottom: 20%;
  animation: 3.5s infinite alternate slideup;
}
.top-right {
  position: absolute;
  top: 2%;
  right: -20px;
  animation: 3s infinite alternate slideupright;
}
@keyframes slideup {
  from {
    bottom: 20%;
  }
  to {
    bottom: 16%;
  }
}
@keyframes slideup-top {
  from {
    top: 8%;
  }
  to {
    top: 5%;
  }
}
@keyframes slideupright {
  from {
    top: 2%;
  }
  to {
    top: 4%;
  }
}
.play-button {
  position: absolute;
  bottom: 200px;
  left: 46%;
}
</style>


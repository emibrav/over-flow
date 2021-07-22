<template>
  <div class="circle">
    <div class="triangle"></div>
  </div>
</template>
<script>
export default {
  name: "PlayButton",
}
</script>
<style scoped>
.circle {
  background-color: #2c2c96;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  position: relative;
  cursor: pointer;
}
.triangle {
  width: 28px;
  border-width: 10px;
  border-color: transparent transparent transparent #fbfefe;
  border-style: solid;
  position: absolute;
  left: 26px;
  bottom: 20px;
}
.circle:hover {
  background-color: #4443cb;
}
</style>

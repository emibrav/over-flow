<template>
  <button class="start-button" :style="[bgColor]">{{ text }}</button>
</template>
<script>
export default {
  name: "StartButton",
  props: {
    text: {
      type: String,
      required: true,
    },
    bgColor: {
      type: String,
      required: true,
    },
  },
}
</script>
<style scoped>
.start-button {
  white-space: nowrap;
  background-color: #2c2c96;
  font-size: 0.8rem;
  font-weight: bold;
  letter-spacing: 1px;
  color: white;
  border-radius: 5px;
  border: none;
  padding: 1rem;
  cursor: pointer;
  text-transform: uppercase;
  transition: 0.5s;
}
.start-button:hover {
  background-color: #3f3faa;
}
</style>

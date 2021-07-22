<template>
  <div class="container">
    <Header class="header"/>
    <hero class="hero" />
    <TechsBar />
    <TurnDesigns />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import TechsBar from "@/components/TechsBar.vue";
import TurnDesigns from "@/components/TurnDesigns.vue";

export default {
  name: "Home",
  components: {
    Header,
    Hero,
    TechsBar,
    TurnDesigns,
  },
};
</script>
<style scoped>
img {
  width: 400px;
  height: 400px;
}
</style>

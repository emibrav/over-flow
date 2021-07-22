/* eslint-disable prettier/prettier */
<template>
  <div class="header" :class="[myScroll > 0 ? 'hola' : '']">
    <div class="second-header">
      <img src="../assets/logo-overflow.svg" alt="logo-overflow" />
      <div class="nav-1">Product &#8595;</div>
      <div class="nav-2">Overflow for &#8595;</div>
      <div class="nav-3">Examples</div>
      <div class="nav-4">Pricing</div>
      <div class="nav-5">Enterprise</div>
    </div>
    <div class="header-right">
      <router-link to="/sign">
        <button class="signin-button">Sign In</button>
      </router-link>
      <button class="start-button">START FOR FREE</button>
    </div>
  </div>
</template>
<script>
export default {
  name: "Header",
  data() {
    return {
      myScroll: window.scrollY,
    };
  },
};
</script>
<style scoped>
.hola {
  border-bottom: 1px solid grey;
}
.header {
  /* border: 1px solid salmon; */
  margin: 0 auto 1rem;
  max-width: 100%;
  padding: 1.5rem 2.5rem 1rem 2.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: white;
  position: fixed;
  right: 0;
  left: 0;
  top: 0;
  z-index: 1030;
}
.second-header {
  display: flex;
}
.nav-1,
.nav-2,
.signin-button,
.start-button {
  white-space: nowrap;
}
.nav-1,
.nav-2,
.nav-3,
.nav-4,
.nav-5 {
  font-size: 1rem;
  padding: 0.5rem 1.2rem 0.5rem 0.7rem;
  cursor: pointer;
  letter-spacing: 0.8px;
}
.nav-1 {
  margin-left: 3rem;
}
.nav-3,
.nav-4,
.nav-5,
.signin-button {
  display: inline-block;
  position: relative;
}
.nav-3::before,
.nav-4::before,
.nav-5::before,
.signin-button::before {
  content: "";
  position: absolute;
  width: 70%;
  transform: scaleX(0);
  height: 0.8px;
  bottom: 0;
  left: 10%;
  background-color: black;
  transform-origin: bottom right;
  transition: transform 0.3s ease-out;
}
.nav-3:hover::before,
.nav-4:hover::before,
.nav-5:hover::before,
.signin-button:hover::before {
  transform: scaleX(1);
  transform-origin: bottom left;
}
.signin-button {
  /* border: 1px solid salmon; */
  border: none;
  width: 80px;
  height: 40px;
  padding: 1.1rem 0rem;
  background-color: unset;
  margin-right: 3rem;
  font-size: 1rem;
  cursor: pointer;
}
.header-right {
  display: flex;
}
.start-button {
  background-color: #2c2c96;
  font-size: 0.8rem;
  font-weight: bold;
  letter-spacing: 1px;
  color: white;
  border-radius: 5px;
  border: none;
  padding: 1rem;
  padding-top: 1.2rem;
  padding-bottom: 1.2rem;
  cursor: pointer;
  transition: 0.5s;
}
.start-button:hover {
  background-color: #3f3faa;
}
</style>

<template>
  <div class="container">
    <div class="left">
      <div class="logo">
        <router-link to="/">
          <img src="../assets/logo-overflow.svg" alt="" />
        </router-link>
      </div>
      <div class="text">
        <p>Communicate your designs like never before.</p>
      </div>
      <div class="imagen">
        <img class="image-1" src="../assets/sign-in.svg" alt="" />
      </div>
    </div>
    <div class="right">
      <div class="title">Sign in</div>
      <form class="form" action="#">
        <div class="user-email">
          <span>Email</span>
          <input
            class="inputs"
            :class="[isCompleted && !email ? 'is-red' : 'border']"
            @blur="isCompleted = true"
            v-model="email"
            type="text"
            placeholder="alex@example.com"
            required
          />
          <!-- <p class="warning">Email address is required</p> -->
          <div class="warning" v-if="isCompleted && !email">
            Must complete email
          </div>
        </div>
        <div class="user-password">
          <div class="span-container">
            <span>Password</span>
            <span class="forgot-pass">Forgot password?</span>
          </div>
          <input
            :class="[isCompletedPass && !password ? 'is-red' : 'border']"
            @blur="isCompletedPass = true"
            v-model="password"
            class="inputs pass"
            type="password"
            required
          />
          <div class="warning" v-if="isCompletedPass && !password">
            This cannot be empty
          </div>
        </div>
        <div class="sign-button-container">
          <button
            class="sign-button"
            :class="[email && password ? 'clickeable' : 'not-clickeable']"
          >
            Sign in
          </button>
        </div>
        <div class="separator">
          <div class="line"></div>
          <div class="separator_line">or</div>
          <div class="line"></div>
        </div>
        <div class="sign-button-google-container">
          <button class="sign-button-google">
            <img class="google-image" src="../assets/google-logo.png" alt="">
            Sign in with Google
          </button>
        </div>
        <div class="other-signs">
          <a class="SSO" href="#">Sign in with SSO</a>
          <br />
          <br />
          <div>
            Don't yout have an account?
            <a href="#">Sign up</a>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  name: "Sign",
  data() {
    return {
      isCompleted: false,
      isCompletedPass: false,
      email: "",
      password: "",
    };
  },
};
</script>
<style scoped>
.is-red {
  border: 1px solid rgba(250, 47, 47, 0.788);
}
.border {
  border: 0.5px solid #cfd2d7;
}
.warning {
  color: red;
  font-size: 0.8rem;
  margin-top: 0.5rem;
  /* display: none; */
}
.clickeable {
  background-color: #0165c5;
  color: white;
  cursor: pointer;
  transition: 0.3s;
}
.clickeable:hover {
  background-color: #2082dd;
}
.container {
  display: flex;
}
.left {
  background-color: #d5f3ff;
  max-width: 500px;
  min-width: 450px;
  position: relative;
}
.image-1 {
  position: absolute;
  bottom: 10%;
}
.logo {
  padding: 1rem;
  position: absolute;
  z-index: 1030;
}
.logo > img {
  height: 25px;
}
.text {
  padding: 1rem;
  position: absolute;
  z-index: 1030;
  top: 10%;
}
.text > p {
  font-family: "Inter var", sans-serif;
  text-align: left;
  font-size: 20px;
  font-weight: bold;
}
.forgot-pass {
  color: #808388;
}
.forgot-pass:hover {
  cursor: pointer;
  text-decoration: underline;
}
.imagen {
  height: 500px;
}
.right {
  /* border: 1px solid burlywood; */
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100%;
  max-width: 70%;
  height: 100vh;
}
.title {
  font-size: 2rem;
  font-weight: bold;
  /* border: 1px solid salmon; */
  margin-top: 5rem 0;
}
.user-email,
.user-password {
  /* border: 1px solid salmon; */
  width: 400px;
  display: flex;
  flex-direction: column;
  margin: 2rem 0;
}
.span-container {
  display: flex;
  justify-content: space-between;
  margin-bottom: 1rem;
  font-size: 15px;
}
/* .border {
  border: 1px solid #cfd2d7;
} */
.inputs {
  height: 37px;
  border-radius: 7px;
  font-size: 1.2rem;
  padding-left: 0.8rem;
}
.inputs::placeholder {
  font-size: 1rem;
  color: #ceccc1;
  /* padding: 0 1rem; */
}
.user-email > span,
.user-password > span {
  font-size: 0.9rem;
  margin-bottom: 0.8rem;
}
.sign-button-container > button {
  width: 400px;
}
.sign-button {
  width: 100%;
  height: 48px;
  border-radius: 5px;
  box-shadow: 1px 2px 2px 1px rgba(0, 0, 0, 0.1);
  /* background-color: #f0f1f3;
  color: #bac0c8; */
  border: none;
  font-size: 1rem;
  font-weight: bolder;
  letter-spacing: 1.5px;
}
.not-clickeable {
  background-color: #f0f1f3;
  color: #bac0c8;
}
.pass {
  letter-spacing: 3px;
}
.sign-button-google {
  width: 100%;
  height: 48px;
  border-radius: 5px;
  box-shadow: 1px 2px 2px 0px rgba(0, 0, 0, 0.1);
  background-color: #f1f1f1;
  border: 1px solid #f0f1f3;
  margin-top: 1rem;
  font-size: 1rem;
  font-weight: bold;
  color: #393b3e;
  letter-spacing: 1px;
  transition: 0.5s;
  cursor: pointer;
}
.sign-button-google:hover {
  box-shadow: 1px 2px 2px 2px rgba(0, 0, 0, 0.1);
}
.other-signs {
  text-align: center;
  font-size: 12px;
  color: #afb1b5;
  margin-top: 2rem;
}
.other-signs > a:hover {
  text-decoration: underline;
}
.other-signs > div > a:hover {
  text-decoration: underline;
}
.SSO {
  margin-bottom: 1rem;
}
a {
  color: #6dadea;
}
.separator {
  display: flex;
  justify-content: space-around;
  margin-top: 2rem;
  position: relative;
}
.separator_line {
  color: rgb(175, 172, 172);
  position: absolute;
  top: -40%;
}
.line {
  /* position: absolute; */
  width: 44%;
  height: 20px;
  border-top: 1px solid rgb(224, 221, 221);
}
.google-image {
  width: 20px;
  height: 20px;
}
@media (max-width: 920px) {
  .left {
    display: none;
  }
  .right {
    max-width: 100%;
  }
}
</style>

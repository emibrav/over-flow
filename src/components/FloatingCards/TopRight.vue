<template>
  <div>
    <div class="photo">
      <img src="../../assets/profile-photo.jpg" alt="" />
    </div>
    <div class="profession">Product owner</div>
  </div>
</template>
<script>
export default {
  name: "TopRight",
}
</script>
<style scoped>
img {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-top: 12%;
}
.photo {
  display: flex;
  justify-content: center;
  background-color: #6464cf;
  /* border: 1px solid salmon; */
  border-radius: 10px;
  width: 65px;
  height: 70px;
  position: relative;
}
.profession {
  /* border: 1px solid salmon; */
  background-color: #2c2c96;
  color: white;
  border-radius: 20px;
  width: 90px;
  height: 30px;
  margin-top: 0.5rem;
  position: absolute;
  left: -3px;
  font-size: 0.6rem;
  letter-spacing: 1px;
  white-space: nowrap;
  font-weight: bold;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 2px 1px 4px 1px rgba(0, 0, 0, 0.2);
}
</style>

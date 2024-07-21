<template>
  <div class="navbar">
    <div class="navbar left">
      <img src="../../assets/Mlogo.png" style="height: 50px" />
    </div>
    <div class="navbar-right">
      <span class="nav-tab"> Home </span>
      <span class="nav-tab"> About </span>
      <span class="nav-tab"> Contact </span>
      <span class="nav-tab" @click="showprojects"> Projects </span>
    </div>
  </div>
</template>

<script setup lan="ts">
import { useRouter } from 'vue-router'
const router = useRouter()
const showprojects = () => {
  router.push('/about');
}
</script>
<style scoped>
.navbar {
  display: flex;
  flex-direction: row;
  background-color: black;
  color: aliceblue;
  align-items: center;
  top: 0;
}

.navbar-right {
  width: 80vw;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>

<template>
  <div class="navbar">
    <div class="navbar-left">
      <img src="../../assets/myicon.png" style="height: 40px" />
    </div>
    <div class="navbar-middle">
      <div class="nav-tab">Home</div>
      <div class="nav-tab">About</div>
      <div class="nav-tab">Contact</div>
      <div class="nav-tab" @click="showprojects">Projects</div>
    </div>
    <div class="navbar-right">
      <span>x</span>
    </div>
  </div>
</template>

<script setup lan="ts">
import { useRouter } from 'vue-router'
const router = useRouter()
const showprojects = () => {
  router.push('/about')
}
</script>
<style scoped>
.navbar {
  display: flex;
  flex-direction: row;
  background-color: rgb(255, 255, 255);
  color: aliceblue;
  align-items: center;
  justify-content: space-between;
  top: 0;
}
.nav-tab {
  color: black;
  width: 150px;
  display:flex;
  align-items: center;
  justify-content: center;
  padding: 5px;
}

.navbar-middle :hover{
  color: aliceblue;
  background-color: black;
  border-radius: 4px;
  cursor: pointer;
}

.navbar-left {
  width: 15vw;
}

.navbar-right {
  width: 15vw;
  display: flex;
  align-items: center;
}

.navbar-middle {
  height: 40px;
  display: flex;
  align-items: center;
}
</style>

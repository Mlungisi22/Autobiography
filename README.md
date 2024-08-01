# Autobiography

<template>
  <div class="navbar">
    <div class="navbar-left">
      <img src="../../assets/myicon.png" style="height: 40px" />
    </div>
    <div class="navbar-middle">
      <div class="nav-tab" @click="goHome">Home</div>
      <div class="nav-tab" @click="showabout">About</div>
      <div class="nav-tab" @click="showResume">resume</div>
      <div class="nav-tab" @click="showcontact">Contact</div>
      <div class="nav-tab" @click="showprojects">Projects</div>
    </div>
    <div class="navbar-right">
      <div class="instagram">
        <img src="../../assets/instagramicon.png" style="height: 40px" @click="gotoInstagram"/>
      </div>
      <div class="github">
        <img src="../../assets/gitIcon.png" style="height: 40px" @click="goToGithub" />
      </div>
      <div class=" linkedIn">
        <img src="../../assets/linkedInIcon.png" style="height: 40px" @click="goToLinkedIn" />
      </div>
    </div>
  </div>
</template>

<script setup lan="ts">
import { useRouter } from 'vue-router'
const router = useRouter()
const showprojects = () => {
  router.push('/projects')
}

const showabout = () => {
  router.push('/about')
}

const showcontact = () => {
  router.push('/projects')
}

const showResume =()=>{
  router.push('/resume');
  console.log("to add resume")
}

const goHome=()=>{
  console.log("tofixhome");
  router.back();
}

const gotoInstagram=()=>{
  window.location.href = "https://www.instagram.com/maxwell_mlungisi";
}
const goToGithub=()=>{
  window.location.href = "https://www.github.com/MLungisi22";
}
const goToLinkedIn=()=>{
  window.location.href = "https://www.LinkedIn.com/in/max-mbuyisa";
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

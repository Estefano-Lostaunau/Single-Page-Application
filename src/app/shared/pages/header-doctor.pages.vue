<template>
  <Toolbar class="p-component p-toolbar-custom">
    <div class="toolbar-content">
      <div class="logo-container">
        <img src="../../../assets/images/logo.png" alt="Logo" class="logo">
        <h1>HormonalCare</h1>
      </div>
      <div class="search-bar-colleague">
      <doctor-view-colleague></doctor-view-colleague>
      </div>
      <span class="spacer"></span>
      <router-link v-for="(option, i) in optionsPatients" :key="i" :to="option.path" class="nav-button" :class="{ 'first-button': i === 0 }">
        <div class="icon-text">
          <img :src="option.icon" alt="option.title" class="option-icon">
        </div>
        {{ option.title }}
      </router-link>
    </div>
  </Toolbar>
  <footer-content />
</template>


<script>

import Toolbar from 'primevue/toolbar';
import logo from '@/assets/images/logo.png';
import calendar from '@/assets/images/calendar.png';
import message from '@/assets/images/message.png';
import bell from '@/assets/images/bell.png';
import homeIcon from '@/assets/images/home-icon.png';
import profileIcon from '@/assets/images/profile-icon.png';
import FooterContent from "@/app/shared/pages/footer-content.pages.vue";
import DoctorViewColleague from "@/app/communications/pages/doctor-view-colleague.vue";
export default {
  name: 'HeaderPatient',
  components: {
    DoctorViewColleague,
    FooterContent,
  },
  data() {
    return {
      logo,
      optionsPatients: [
        { path: '/homeDoctor', title: 'Home', icon: homeIcon},
        { path: '/calendar', title: 'Calendar', icon: calendar},
        { path: '/messages', title: 'Messages', icon: message},
        { path: '/notifications', title: 'Notifications', icon: bell},
        { path: '/doctorProfile', title: 'Profile', icon: profileIcon},
      ]

    }
  }
}
</script>



<style scoped>
.toolbar-content {
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #A788AB;
  width: 100%;

  padding:  0 40px;
}

.logo-container {
  display: flex;
  align-items: center;
}

.logo-container .logo {
  border-radius: 60%;
  width: 50px;
  height: 50px;
  margin-right: 10px;
}

.p-toolbar-custom {
  box-sizing: border-box;
  background-color: #A788AB;
  height: 60px;
  width: 100%;
  margin-right: 40px;
}

.spacer {
  flex: 1 1 auto;
}

.icon-text {
  top: 8px;
  position: relative;
  display: inline-block;
  margin-left: 0;
}

.option-icon {
  height: 30px;
  margin-right: 10px;
}

.first-button {
  margin-left: 20px;
}

.nav-button {
  margin-left: 44px;
}
.search-bar-colleague{
  display: flex;
  margin-left: 25px;
}
</style>

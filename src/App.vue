<script>
import homePatient from './app/profiles/pages/patient-profile/home-patient.pages.vue';
import patientProfile from './app/profiles/pages/patient-profile/patient-profile.pages.vue';
import headerDoctor from './app/shared/pages/header-doctor.pages.vue';
import FooterContent from "./app/shared/pages/footer-content.pages.vue";
import DoctorRegistration from "./app/identity-and-access/pages/doctor-registration.pages.vue";
import SelectUserRole from './app/identity-and-access/pages/select-user-role.pages.vue';
import userTypeService from "@/app/shared/services/user-type.service";
import HeaderForUserTypeService from "@/app/shared/components/header-for-user-type-services.vue";
import DoctorPatientPages from "@/app/communications/pages/doctor-patient.pages.vue";
import PatientDoctorPages from "@/app/communications/pages/patient-doctor.pages.vue";
export default {
  components: {
    SelectUserRole,
    DoctorRegistration,
    FooterContent,
    homePatient,
    patientProfile,
    headerDoctor,
    HeaderForUserTypeService,
    DoctorPatientPages,
    PatientDoctorPages
  },
  computed: {
    userType() {
      return userTypeService.userType.value;
    },
  }
};

</script>

<template>


  <!-- <header-doctor></header-doctor>-->

   <!--<doctor-registration></doctor-registration>-->

 <!--<select-user-role> </select-user-role>-->

      <header-for-user-type-service></header-for-user-type-service>
      <router-view></router-view>

  <!--<doctor-patient-pages></doctor-patient-pages>-->
  <!-- <PatientDoctorPages></PatientDoctorPages>-->

    <!--<homePatient></homePatient>-->
  <!--<patientProfile></patientProfile>-->

  </template>


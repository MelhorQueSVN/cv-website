<template>
      <v-col cols="12" class="aboutMefirstColColor" md="4">
          
          <v-avatar size="130">
            <v-img
                :src="require('@/assets/pictures/face.jpg')"
            ></v-img>
          </v-avatar>
          <h2 class="aboutMeTextColor"> João <span class="blue--text">Nunes</span> </h2>
          <h2 class="aboutMeTextColor"> An aspiring web developer </h2>
          
          <GenInfo />

          <Social />

          <Activities />

          <InterSkills />

          <Languages />

      </v-col>      
</template>

<script>
import GenInfo from '@/components/aboutme/sidebar/GenInfo.vue'
import Social from '@/components/aboutme/sidebar/Social.vue'
import Activities from '@/components/aboutme/sidebar/Activities.vue'
import InterSkills from '@/components/aboutme/sidebar/InterSkills.vue'
import Languages from '@/components/aboutme/sidebar/Languages.vue'

export default {
  components : { 
    GenInfo, 
    Social, 
    Activities,
    InterSkills, 
    Languages
  }

}
</script>


<style scoped src="@/assets/styles/styles.css">
</style>
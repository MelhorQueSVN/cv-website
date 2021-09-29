<template>
      <v-col cols="12" class="aboutMefirstColColor" md="4">
          
          <v-avatar size="130">
            <v-img
                :src="require('@/assets/pictures/face.jpg')"
                :lazy-src="require('@/assets/pictures/face.jpg')"
            >
                <template v-slot:placeholder>
                  <v-row
                    class="fill-height ma-0"
                    align="center"
                    justify="center"
                  >
                    <v-progress-circular
                      indeterminate
                      color="grey lighten-5"
                    ></v-progress-circular>
                </v-row>
              </template>
           </v-img>      
          </v-avatar>
          
          <h2 class="aboutMeTextColor"> João <span class="blue--text">Nunes</span> </h2>
          <h2 class="aboutMeTextColor"> {{ $t('aboutme.aspiring') }} </h2>
          
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
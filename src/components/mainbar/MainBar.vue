<template>
    <v-col cols="12" class="aboutMesecondColColor" md="7">
                        
        <AboutMe />                

        <Education />

        <Experience />

        <Skills /> 
                          
    </v-col>  
</template>

<script>
import AboutMe from '@/components/mainbar/AboutMe.vue' 
import Education from '@/components/mainbar/Education.vue'
import Experience from '@/components/mainbar/Experience.vue'

export default {
    components : { 
        AboutMe, 
        Education, 
        Experience
    }
}
</script>

<style scoped src="@/assets/styles/styles.css">
</style>
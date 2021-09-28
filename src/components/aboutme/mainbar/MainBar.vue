<template>
    <v-col cols="12" class="aboutMesecondColColor" md="7">
                        
        <AboutMe />                

        <Education />

        <Experience />

        <Skills /> 

    </v-col>  
</template>

<script>
import AboutMe from '@/components/aboutme/mainbar/AboutMe.vue' 
import Education from '@/components/aboutme/mainbar/Education.vue'
import Experience from '@/components/aboutme/mainbar/Experience.vue'
import Skills from '@/components/aboutme/mainbar/Skills.vue'

export default {
    components : { 
        AboutMe, 
        Education, 
        Experience, 
        Skills
    }
}
</script>

<style scoped src="@/assets/styles/styles.css">
</style>
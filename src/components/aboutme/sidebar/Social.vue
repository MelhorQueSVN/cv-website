<template>
    <div>          
        <h3 class="aboutMeTextColor text-left pt-6"> {{ $t('aboutme.sidebar.social.findme') }} </h3>
        <v-divider class="dividerColorWhite"> </v-divider>
        <v-row> 
            
            <v-col> 
            <v-btn icon color="white" href="https://github.com/MelhorQueSVN" target="_blank">  
                <v-icon size="30"> mdi-github</v-icon>
            </v-btn>
            </v-col>
            <v-col> 
            <v-btn icon color="white" href="https://www.linkedin.com/in/jo%C3%A3o-nunes-11031b222/" target="_blank">  
                <v-icon size="30"> mdi-linkedin</v-icon>
            </v-btn>
            </v-col>
        </v-row>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped src="@/assets/styles/styles.css">
</style>
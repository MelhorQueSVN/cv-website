<template>
    <div>
        <h3 class="aboutMeTextColor text-left pt-3"> Interpersonal skills </h3>
        <v-divider class="dividerColorWhite"> </v-divider>
          
          <v-row class="pt-3">      
              <v-col cols="12" md="4">                          
                <v-btn color="white" small outlined rounded>
                  {{ $t('aboutme.sidebar.interskills.responsability') }}
                </v-btn>                                                     
              </v-col>
              
              <v-col cols="12" md="8">       
                <v-btn color="white" small outlined rounded>
                  {{ $t('aboutme.sidebar.interskills.collaborator') }}
                </v-btn>                  
              </v-col>      
          </v-row>
          
          <v-row>                          
              <v-col cols="12" md="4">                          
                <v-btn color="white" small outlined rounded>
                  {{ $t('aboutme.sidebar.interskills.communicator') }}
                </v-btn>                                                     
              </v-col>
              
              <v-col cols="12" md="8">       
                <v-btn color="white" small outlined rounded>
                  {{ $t('aboutme.sidebar.interskills.feedback') }}
                </v-btn>                  
              </v-col>
          </v-row>
          
          <v-row>                        
              <v-col cols="12" md="6">                          
                <v-btn color="white" small outlined rounded>
                  {{ $t('aboutme.sidebar.interskills.flexible') }}
                </v-btn>                                                     
              </v-col>
              
              <v-col cols="12" md="6">       
                <v-btn color="white" small outlined rounded>
                  {{ $t('aboutme.sidebar.interskills.humor') }}
                </v-btn>                  
              </v-col>                       
          </v-row>
          
          <v-row>                        
              <v-col cols="12" md="4">                          
                <v-btn color="white" small outlined rounded>
                  {{ $t('aboutme.sidebar.interskills.listener') }}
                </v-btn>                                                     
              </v-col>
              
              <v-col cols="12" md="6">       
                <v-btn color="white" small outlined rounded>
                  {{ $t('aboutme.sidebar.interskills.patient') }}
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
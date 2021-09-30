<template>
    <div>
        <h3 class="aboutMeTextColor text-left pt-3"> Interpersonal skills </h3>
        <v-divider class="dividerColorWhite"> </v-divider>
          
          <v-row class="pt-3">      

              <v-col cols="12" md="6">       
                <h4 class="white--text">
                  {{ $t('aboutme.sidebar.interskills.feedback') }}
                </h4>                  
              </v-col>


              <v-col cols="12" md="6">                          
                <h4 class="white--text"> 
                  {{ $t('aboutme.sidebar.interskills.responsability') }} 
                </h4>                                             
              </v-col>     
          </v-row>
          
          <v-row>                          
              <v-col cols="12" md="5">                          
                <h4 class="white--text">
                  {{ $t('aboutme.sidebar.interskills.communicator') }}
                </h4>                                                     
              </v-col>

              <v-col cols="12" md="7">       
                <h4 class="white--text">
                  {{ $t('aboutme.sidebar.interskills.collaborator') }}
                </h4>                 
              </v-col>   

          </v-row>
          
          <v-row>                        
              <v-col cols="12" md="6">                          
                <h4 class="white--text">
                  {{ $t('aboutme.sidebar.interskills.flexible') }}
                </h4>                                                     
              </v-col>
              
              <v-col cols="12" md="6">       
                <h4 class="white--text">
                  {{ $t('aboutme.sidebar.interskills.humor') }}
                </h4>                  
              </v-col>                       
          </v-row>
          
          <v-row>                        
              
              <v-col cols="12" md="6">       
                <h4 class="white--text">
                  {{ $t('aboutme.sidebar.interskills.patient') }}
                </h4>                  
              </v-col>   

              <v-col cols="12" md="6">                          
                <h4 class="white--text">
                  {{ $t('aboutme.sidebar.interskills.listener') }}
                </h4>                                                     
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
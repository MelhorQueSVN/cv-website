<template>
    <div> 
      
      <h3 class="aboutMeTextColor text-left pt-3"> {{ $t('aboutme.sidebar.activity.title') }} </h3>
      <v-divider class="dividerColorWhite"> </v-divider> 
      
      <!-- 1a fila de hobbies -->
      <v-row class="pt-3"> 
        
        <v-col class="pr-0 pl-0"> 
          <v-btn color="white" small outlined rounded>
            <v-icon left>
              mdi-book-open-page-variant
            </v-icon>
             {{ $t('aboutme.sidebar.activity.reading') }}
          </v-btn>
        </v-col> 
        
        <v-col class="pr-0 pl-0"> 
          <v-btn color="white" small outlined rounded>
            <v-icon left>
              mdi-dumbbell
            </v-icon>
             {{ $t('aboutme.sidebar.activity.training') }}
          </v-btn>
        </v-col> 
        
        <v-col class="pr-0 pl-0"> 
          <v-btn color="white" small outlined rounded>
            <v-icon left>
              mdi-music
            </v-icon>
             {{ $t('aboutme.sidebar.activity.music') }}
          </v-btn>
        </v-col> 
        
        <v-col class="pr-0 pl-0"> 
          <v-btn color="white" small outlined rounded>
            <v-icon left>
              mdi-gamepad
            </v-icon>
             {{ $t('aboutme.sidebar.activity.games') }}
          </v-btn>
        </v-col> 
      
      </v-row>
      
      <!-- 2a fila de hobbies -->
      <v-row> 
        
        <v-col class="pr-0 pl-0"> 
          <v-btn color="white" small outlined rounded>
            <v-icon left>
              mdi-hiking
            </v-icon>
             {{ $t('aboutme.sidebar.activity.hiking') }}
          </v-btn>
        </v-col> 
        
        <v-col class="pr-0 pl-0"> 
          <v-btn color="white" small outlined rounded>
            <v-icon left>
              mdi-file-document-edit
            </v-icon>
              {{ $t('aboutme.sidebar.activity.projects') }}
          </v-btn>
        </v-col> 
        
        <v-col class="pr-0 pl-0"> 
          <v-btn color="white" small outlined rounded>
            <v-icon left>
              mdi-movie-open
            </v-icon>
             {{ $t('aboutme.sidebar.activity.movies') }}
          </v-btn>
        </v-col> 
        
        <v-col class="pr-0 pl-0"> 
          <v-btn color="white" small outlined rounded>
            <v-icon left>
              mdi-basketball
            </v-icon>
             {{ $t('aboutme.sidebar.activity.sports') }}
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
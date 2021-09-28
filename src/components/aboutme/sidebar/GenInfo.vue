<template>
    <div>  
      
      <h3 class="aboutMeTextColor text-left pt-6"> Info </h3>
      <v-divider class="dividerColorWhite"> </v-divider>
      
      <!-- EMAIL -->
      <v-row class="pt-3" align="center">
        <!-- Temos uma row dividida numa coluna para o icon seguido de outra coluna dividida em 2 rows, em ecrãs pequenos e grandes 20% vai para o col icon -->
        <!-- e 80% é dedicada à col que contem os dados -->
        <v-col cols="2" md="2" class="text-left"> 
              <v-icon
                large
                color="white"
              >
                mdi-email
              </v-icon>
        </v-col> 
        
        <v-col cols="10" md="10" class="text-left aboutMeTextColor">
          <v-row align="center">
            Email
          </v-row> 
          <v-row align="center">
            joaonunes.22.12@gmail.com
          </v-row> 
        </v-col>                    
      </v-row>
   
      <!-- WEBSITE -->
      <v-row class="pt-3" align="center">
        <!-- Temos uma row dividida numa coluna para o icon seguido de outra coluna dividida em 2 rows, em ecrãs pequenos e grandes 20% vai para o col icon -->
        <!-- e 80% é dedicada à col que contem os dados -->
        <v-col cols="2" md="2" class="text-left"> 
              <v-icon
                large
                color="white"
              >
                mdi-search-web
              </v-icon>
        </v-col> 
        
        <v-col cols="10" md="10" class="text-left aboutMeTextColor">
          <v-row align="center">
            Website
          </v-row> 
          <v-row align="center">
            joao-nunes-cv.pt
          </v-row> 
        </v-col>                    
      </v-row>
      
      <!-- NASCIMENTO -->
      <v-row class="pt-3" align="center">
        <!-- Temos uma row dividida numa coluna para o icon seguido de outra coluna dividida em 2 rows, em ecrãs pequenos e grandes 20% vai para o col icon -->
        <!-- e 80% é dedicada à col que contem os dados -->
        <v-col cols="2" md="2" class="text-left"> 
              <v-icon
                large
                color="white"
              >
                mdi-cake-variant
              </v-icon>
        </v-col> 
        
        <v-col cols="10" md="10" class="text-left aboutMeTextColor">
          <v-row align="center">
            Birthday
          </v-row> 
          <v-row align="center">
            22 November 1998
          </v-row> 
        </v-col>                    
      </v-row>
      
      <!-- LOCALIZAÇÃO -->
      <v-row class="pt-3" align="center">
        <!-- Temos uma row dividida numa coluna para o icon seguido de outra coluna dividida em 2 rows, em ecrãs pequenos e grandes 20% vai para o col icon -->
        <!-- e 80% é dedicada à col que contem os dados -->
        <v-col cols="2" md="2" class="text-left"> 
              <v-icon
                large
                color="white"
              >
                mdi-map-marker
              </v-icon>
        </v-col> 
        
        <v-col cols="10" md="10" class="text-left aboutMeTextColor">
          <v-row align="center">
            Location
          </v-row> 
          <v-row align="center">
            Lousada, Portugal
          </v-row> 
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
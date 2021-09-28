<template>
    <div>
        <!-- Acerca de mim-->
        <v-row> 
              <v-col class="text-left"> 
                  <h4> {{ $t('aboutme.mainbar.aboutme.title') }} </h4>
              </v-col>
            </v-row> 
            <!-- Consoante o tamanho do ecrã muda o width -->
            <v-divider v-if="$vuetify.breakpoint.smAndDown" width="30%" > </v-divider> 
            <v-divider v-else width="10%" > </v-divider> 
            
            <v-row class="pt-6"> 
              <v-col class="text-left"> 
                  <p> {{ $t('aboutme.mainbar.aboutme.first_par') }} </p>
                  <p> {{ $t('aboutme.mainbar.aboutme.second_par') }} </p>
                  <p> {{ $t('aboutme.mainbar.aboutme.third_par') }} </p>
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
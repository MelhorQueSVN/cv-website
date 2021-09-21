<template>
  <div class="home">
      
      <section id="hero">             
        <v-row no-gutters>
          <v-img
            :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
           :src="require('@/assets/splash-1.jpg')"
          >

            <Navbar />

            <v-theme-provider dark>
              <v-container fill-height>
                <v-row
                  align="center"
                  class="white--text mx-auto"
                  justify="center"
                >
                  <v-col
                    class="white--text text-center"
                    cols="12"
                    tag="h1"
                  >
                    <span
                    :class="[$vuetify.breakpoint.smAndDown ? 'display-3' : 'display-4']"
                     class="font-weight-black"
                    >
                      João Nunes
                    </span>

                    <br>

                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-1': 'display-2']"
                      class="font-weight-light"
                    >
                      Software Engineer Student at Universidade do Minho <br>
                    </span> 

                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-0': 'display-1']"
                      class="font-weight-light"
                    >
                      Hi I'm João Nunes and I'm currently finishing my masters degree and Universidade do Minho
                    </span> 

                  </v-col>
                  
                  <v-btn
                    class="align-self-end"
                    fab
                    outlined
                    @click="$vuetify.goTo('#about-me')"
                  >
                    <v-icon>mdi-chevron-double-down</v-icon>
                  </v-btn>
                
                </v-row>
              </v-container>
            </v-theme-provider>
          </v-img>
        </v-row>
      </section>

      <section id="about-me">
          <!-- Adiciona padding em cima e baixo --> 
          <div class="pt-12 pb-12"> 
              <v-container class="text-center">
                  
                  <v-row> 

                    <v-col cols="4" class="aboutMefirstColColor">

                      <v-avatar size="130">
                        <v-img
                            class="elevation-6"
                            :src="require('@/assets/default-pic.png')"
                        ></v-img>
                      </v-avatar>

                      <h2 class="white--text"> João <span class="blue--text">Nunes</span> </h2>
                      <h2 class="white--text"> An aspiring web developer </h2>

                    </v-col>

                    <v-col cols="8" class="aboutMesecondColColor">
                      merda
                    </v-col>

                  </v-row>

              </v-container> 
          </div>
      
      </section>

  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'

export default {
  name: 'Home',
  components : { 
    Navbar
  }

}
</script> 


<style scoped>

.aboutMefirstColColor { 
  background-color: #3c3c3c;
}

.aboutMesecondColColor { 
  background-color: #d8d8d8;
}

</style>

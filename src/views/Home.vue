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
                    
                    <!-- v-col não tem xs, portanto com cols="12" faz fill do ecrã, depois devices com md para cima fica apenas com 4 -->
                    <v-col cols="12" class="aboutMefirstColColor" md="4">

                      <v-avatar size="130">
                        <v-img
                            class="elevation-6"
                            :src="require('@/assets/default-pic.png')"
                        ></v-img>
                      </v-avatar>

                      <h2 class="aboutMeTextColor"> João <span class="blue--text">Nunes</span> </h2>
                      <h2 class="aboutMeTextColor"> An aspiring web developer </h2>

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

                      <h3 class="aboutMeTextColor text-left pt-6"> You can also find me on </h3>
                      <v-divider class="dividerColorWhite"> </v-divider>

                      <v-row> 
                        
                        <v-col> 
                          <v-btn icon color="white" href="https://github.com/MelhorQueSVN" target="_blank">  
                            <v-icon> mdi-github</v-icon>
                          </v-btn>
                        </v-col>

                        <v-col> 
                          <v-btn icon color="white" href="https://pt.linkedin.com/" target="_blank">  
                            <v-icon> mdi-linkedin</v-icon>
                          </v-btn>
                        </v-col>

                        <v-col> 
                          <v-btn icon color="white" href="https://www.facebook.com/joao.filipe.16940/" target="_blank">  
                            <v-icon> mdi-facebook</v-icon>
                          </v-btn>
                        </v-col>

                        <v-col> 
                          <v-btn icon color="white" href="https://www.instagram.com/joaoflpnunes/" target="_blank">  
                            <v-icon> mdi-instagram</v-icon>
                          </v-btn>
                        </v-col>

                      </v-row>

                      <h3 class="aboutMeTextColor text-left pt-3"> Things I enjoy in my free time </h3>
                      <v-divider class="dividerColorWhite"> </v-divider> 

                      <!-- 1a fila de hobbies -->
                      <v-row class="pt-3"> 

                        <v-col class="pr-0 pl-0"> 
                          <v-btn color="white" small outlined rounded>
                            <v-icon left>
                              mdi-book-open-page-variant
                            </v-icon>
                             Reading
                          </v-btn>
                        </v-col> 

                        <v-col class="pr-0 pl-0"> 
                          <v-btn color="white" small outlined rounded>
                            <v-icon left>
                              mdi-dumbbell
                            </v-icon>
                             Training
                          </v-btn>
                        </v-col> 

                        <v-col class="pr-0 pl-0"> 
                          <v-btn color="white" small outlined rounded>
                            <v-icon left>
                              mdi-music
                            </v-icon>
                             Music
                          </v-btn>
                        </v-col> 

                        <v-col class="pr-0 pl-0"> 
                          <v-btn color="white" small outlined rounded>
                            <v-icon left>
                              mdi-gamepad
                            </v-icon>
                             Games
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
                             Hiking
                          </v-btn>
                        </v-col> 

                        <v-col class="pr-0 pl-0"> 
                          <v-btn color="white" small outlined rounded>
                            <v-icon left>
                              mdi-file-document-edit
                            </v-icon>
                              Projects
                          </v-btn>
                        </v-col> 

                        <v-col class="pr-0 pl-0"> 
                          <v-btn color="white" small outlined rounded>
                            <v-icon left>
                              mdi-movie-open
                            </v-icon>
                             Movies
                          </v-btn>
                        </v-col> 

                        <v-col class="pr-0 pl-0"> 
                          <v-btn color="white" small outlined rounded>
                            <v-icon left>
                              mdi-basketball
                            </v-icon>
                             Sports
                          </v-btn>
                        </v-col> 

                      </v-row>

                      <h3 class="aboutMeTextColor text-left pt-3"> Languages </h3>
                      <v-divider class="dividerColorWhite"> </v-divider> 

                      <v-row class="pt-3"> 

                        <v-col>
                          <v-progress-circular
                            :rotate="90"
                            :size="100"
                            :width="15"
                            :value="valuePt"
                            color="blue"
                          >
                            {{ valuePt }}
                          </v-progress-circular>
                          <p class="aboutMeTextColor pt-2"> Fluent Portuguese </p>
                        </v-col>

                        <v-col>
                          <v-progress-circular
                            :rotate="90"
                            :size="100"
                            :width="15"
                            :value="valueEn"
                            color="red"
                          >
                            {{ valueEn }}
                          </v-progress-circular>
                          <p class="aboutMeTextColor pt-2"> Advanced English (CAE) </p>
                        </v-col>

                        <v-col>
                          <v-progress-circular
                            :rotate="90"
                            :size="100"
                            :width="15"
                            :value="valueSp"
                            color="yellow"
                          >
                            {{ valueSp }}
                          </v-progress-circular>
                          <p class="aboutMeTextColor pt-2"> Spanish </p>
                        </v-col>

                      </v-row>

                   
                    </v-col>

                    <v-col cols="12" class="aboutMesecondColColor" md="8">

                        <v-row> 
                          <v-col class="text-left"> 
                              <h4> About Me </h4>
                          </v-col>
                        </v-row> 
                        <!-- Consoante o tamanho do ecrã muda o width -->
                        <v-divider v-if="$vuetify.breakpoint.smAndDown" width="30%" class="dividerColorBlack"> </v-divider> 
                        <v-divider v-else width="10%" class="dividerColorBlack"> </v-divider> 
                        
                        <v-row class="pt-6"> 
                          <v-col class="text-left"> 
                              <p> My name is João Nunes, and I'm a software developer currently finishing masters degree in Informatics Engineering at Universidade do Minho in Portugal.</p>
                              <p> I opted to choose Intelligent Systems as well as Knowledge Engineering as my Msc profiles. The first profile can be characterized as a machine learning course, 
                                where a lot of focus was given to the standard machine learning algorithms wether they be supervised or unsupervised. As well as machine learning, the profile also 
                                focused on the creation of multiagent systems, where communication between agents was imperious. The second profile essentialy focused on teaching the principles in 
                                database exploration and administration. 
                              </p>
                              <p>
                                  In regards to my thesis, which I'm currently finishing it, the goal of my thesis is to develop an extraction tool, using machine learning, in order to filter all the desired 
                                  data from various documents. After extracting the data, the data is strucutured in the form of an ontology. A simple website was then constructed in order to query
                                  all the data within the ontology.
                              </p>
                          </v-col>
                        </v-row> 

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
  }, 
  data () {
      return {
        intervalPt: {},
        intervalEn : {},
        intervalSp : {},
        valuePt: 0,
        valueEn : 0, 
        valueSp : 0
      }
    },
    beforeDestroy () {
      clearInterval(this.intervalPt)
      clearInterval(this.intervalEn)
      clearInterval(this.intervalSp)
    },
    mounted () {
      this.intervalPt = setInterval(() => {
        if (this.valuePt === 100) {
          return (this.valuePt = 100)
        }
        this.valuePt += 10
      }, 800)

      this.intervalEn = setInterval(() => {
        if (this.valueEn === 90) {
          return (this.valueEn = 90)
        }
        this.valueEn += 10
      }, 800)

      this.intervalSp = setInterval(() => {
        if (this.valueSp === 30) {
          return (this.valueSp = 30)
        }
        this.valueSp += 10
      }, 800)
    
    },

}
</script> 


<style scoped>

.aboutMefirstColColor { 
  background-color: #3c3c3c;
}

.aboutMesecondColColor { 
  background-color: #d8d8d8;
} 

.aboutMeTextColor { 
  color : white
}

.dividerColorWhite {
    border-color: rgb(255, 252, 252) !important; 
}

.dividerColorBlack {
    border-color: rgb(0, 0, 0) !important; 
}



</style>

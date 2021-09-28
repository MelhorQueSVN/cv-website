<template>
  <div class="home">
      
      <section id="hero">     
        <v-row no-gutters> 
          
          <!-- Só para dar fill -->
          <v-img
            :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"   
          >

          <Navbar />
          
          <v-container fill-height>
            <v-row>
                <v-col cols="12" md="12" justify="center" align="center">
                  <span
                    :class="[$vuetify.breakpoint.smAndDown ? 'display-3' : 'display-4']"
                    class="font-weight-black"
                  >
                    João Nunes <br>
                  </span>

                  <div class="pt-3">      
                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-1': 'display-2']"
                      class="font-weight-light"
                    >
                      {{ $t('home.subtitle') }} <br>
                    </span>
                  </div>
                  
                  <div class="pt-3">        
                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-0': 'display-1']"
                      class="font-weight-light"
                    >
                     {{ $t('home.subsubtitle') }} <br>
                    </span>
                  </div>

                  <div class="pt-3">  
                    <v-btn
                      class="align-self-end"
                      fab
                      outlined
                      @click="$vuetify.goTo('#about-me')"
                    >
                      <v-icon>mdi-chevron-double-down</v-icon>
                    </v-btn>
                  </div>
                </v-col>
             
            </v-row>
         
          </v-container>
          </v-img>
        
        </v-row>
      </section>

      <section id="about-me">
          <!-- Adiciona padding em cima, ou seja, para ecrãs pequenos não usa padding, para ecrãs maiores (md) para cima usa 12 de padding no top --> 
          <!-- Vue escolhe sempre o mais específico para o dispositivo em causa -->
          <div class="pt-0 pt-md-12"> 
              <v-container class="text-center">
                  
                  <v-row justify="center"> 
                    
                    <!-- v-col não tem xs, portanto com cols="12" faz fill do ecrã, depois devices com md para cima fica apenas com 4 -->
                    <SideBar />

                    <MainBar /> 

                  </v-row>
            </v-container> 
          </div>     
      </section>

      <section id="works"> 
          <v-container>
            
            <v-row justify="center">
            
              <Gallery />
            
            </v-row>
          
          </v-container>
      </section>


      <section id="contact"> 
          <v-container>          
            <v-row justify="center">
              
              <Contact />

            </v-row>
          </v-container>
      </section>


      <section id="ending"> 
        <v-row no-gutters> 
          
          <!-- Só para dar fill -->
          <v-img
            :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"   
          >
          
          <v-container fill-height>
            <v-row>
                <v-col cols="12" md="12" justify="center" align="center">
                  <span
                    :class="[$vuetify.breakpoint.smAndDown ? 'display-3' : 'display-4']"
                    class="font-weight-black"
                  >
                    {{ $t('ending.title') }} <br>
                  </span>
                  
                  <div class="pt-3">        
                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-0': 'display-1']"
                      class="font-weight-light"
                    >
                      {{ $t('ending.subtitle') }} <br>
                    </span>
                  </div>

                  <div class="pt-3">        
                    
                    <v-btn text href="CV_JoaoNunes_Pt.pdf" download> 
                      Português 
                      <v-icon right>
                        mdi-file-pdf-box 
                      </v-icon>
                    </v-btn>
                    
                    <v-btn text href="CV_JoaoNunes_En.pdf" download> 
                      English
                      <v-icon right>
                        mdi-file-pdf-box 
                      </v-icon> 
                    </v-btn>
                  
                  </div>

                  <div class="pt-3">  
                    <v-btn
                      class="align-self-end"
                      fab
                      outlined
                      @click="$vuetify.goTo('#hero')"
                    >
                      <v-icon>mdi-chevron-double-up</v-icon>
                    </v-btn>
                  </div>
                </v-col>
             
            </v-row>
         
          </v-container>
          </v-img>
        
        </v-row>
      </section>


  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import SideBar from '@/components/aboutme/sidebar/SideBar.vue'
import MainBar from '@/components/aboutme/mainbar/MainBar.vue'
import Gallery from '@/components/Gallery.vue'
import Contact from '@/components/contact/Contact.vue'

export default {
  name: 'Home',
  components : { 
    Navbar, 
    SideBar, 
    MainBar, 
    Gallery, 
    Contact
  }, 
}
</script> 


<style scoped src="@/assets/styles/styles.css">
</style>

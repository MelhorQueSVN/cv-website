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
                      Software Engineer Student at Universidade do Minho <br>
                    </span>
                  </div>
                  
                  <div class="pt-3">        
                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-0': 'display-1']"
                      class="font-weight-light"
                    >
                      Hi I'm João Nunes and I'm currently finishing my masters degree and Universidade do Minho <br>
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

                    <v-col cols="12" class="aboutMesecondColColor" md="7">
                        
                        <!-- Acerca de mim-->
                        <v-row> 
                          <v-col class="text-left"> 
                              <h4> About Me </h4>
                          </v-col>
                        </v-row> 
                        <!-- Consoante o tamanho do ecrã muda o width -->
                        <v-divider v-if="$vuetify.breakpoint.smAndDown" width="30%" > </v-divider> 
                        <v-divider v-else width="10%" > </v-divider> 
                        
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
                    
                        <!-- Educação -->
                        <v-row> 
                          <v-col class="text-left"> 
                              <h4> Education </h4>
                          </v-col>
                        </v-row> 
                        <!-- Consoante o tamanho do ecrã muda o width -->
                        <v-divider v-if="$vuetify.breakpoint.smAndDown" width="30%" > </v-divider> 
                        <v-divider v-else width="10%" > </v-divider> 
                        
                        <v-row class="pt-6"> 
                          <v-col cols="4" md="2" class="text-left"> 
                            <p> 2013-2016 </p>
                          </v-col>

                          <v-col cols="8" md="10" class="text-left"> 
                            <p> Escola Básica e Secundária de Lustosa </p> 
                            <p> Sciences and Technologies </p>
                          </v-col>                     
                        </v-row> 

                        <v-row class="mt-0"> 
                          <v-col cols="4" md="2" class="text-left"> 
                            <p> 2016-present </p>
                          </v-col>

                          <v-col cols="8" md="10" class="text-left"> 
                            <p> Universidade do Minho </p> 
                            <p> Integrated Masters Degree in Informatics Engineering </p>
                          </v-col>                     
                        </v-row> 


                        <!-- Skills -->
                        <v-row> 
                          <v-col class="text-left"> 
                              <h4> Skills and Main Expertize </h4>
                          </v-col>
                        </v-row> 
                        <!-- Consoante o tamanho do ecrã muda o width -->
                        <v-divider v-if="$vuetify.breakpoint.smAndDown" width="70%" > </v-divider> 
                        <v-divider v-else width="25%" > </v-divider> 
                        
                        <!-- Em ecrãs pequenos cada coluna ocupa o tamanho todo, em ecrãs maiores ocupa 50%-->
                        <v-row class="pt-6 text-left"> 
                          <v-col cols="12" md="6">
                              <p> Java </p>
                              <v-progress-linear color="red" height="25" :value="valueJava"> <strong class="aboutMeTextColor"> {{valueJava + "%"}} </strong> </v-progress-linear>
                          </v-col> 
                          
                          <v-col cols="12" md="6"> 
                              <p> Javascript </p>
                               <v-progress-linear color="yellow accent-3" height="25" :value="valueJavascript"> <strong class="aboutMeTextColor"> {{valueJavascript + "%"}} </strong> </v-progress-linear>                         
                          </v-col>

                          <v-col cols="12" md="6"> 
                              <p> VueJs </p>
                               <v-progress-linear color="green" height="25" :value="valueVueJs"> <strong class="aboutMeTextColor"> {{valueVueJs + "%"}} </strong> </v-progress-linear>                         
                          </v-col>

                          <v-col cols="12" md="6"> 
                              <p> React Native </p>
                               <v-progress-linear color="light-blue" height="25" :value="valueReactN"> <strong class="aboutMeTextColor"> {{valueReactN + "%"}} </strong> </v-progress-linear>                         
                          </v-col>

                          <v-col cols="12" md="6"> 
                              <p> NodeJs </p>
                               <v-progress-linear color="green lighten-2" height="25" :value="valueNodeJs"> <strong class="aboutMeTextColor"> {{valueNodeJs + "%"}} </strong> </v-progress-linear>                         
                          </v-col>
                         
                          <v-col cols="12" md="6"> 
                              <p> Python </p>
                               <v-progress-linear color="blue darken-4" height="25" :value="valuePython"> <strong class="aboutMeTextColor"> {{valuePython + "%"}} </strong> </v-progress-linear>                         
                          </v-col>

                          <v-col cols="12" md="6"> 
                              <p> C/C++ </p>
                               <v-progress-linear height="25" :value="valueC"> <strong class="aboutMeTextColor"> {{valueC + "%"}} </strong> </v-progress-linear>                         
                          </v-col>

                          <v-col cols="12" md="6"> 
                              <p> Cypher </p>
                               <v-progress-linear height="25" :value="valueCy"> <strong class="aboutMeTextColor"> {{valueCy + "%"}} </strong> </v-progress-linear>                         
                          </v-col>

                          <v-col cols="12" md="6"> 
                              <p> Mongo </p>
                               <v-progress-linear color="green" height="25" :value="valueMongo"> <strong class="aboutMeTextColor"> {{valueMongo + "%"}} </strong> </v-progress-linear>                         
                          </v-col>

                          <v-col cols="12" md="6"> 
                              <p> Sql </p>
                               <v-progress-linear color="orange lighten-2" height="25" :value="valueSql"> <strong class="aboutMeTextColor"> {{valueSql + "%"}} </strong> </v-progress-linear>                         
                          </v-col>
                        </v-row>                    
                    </v-col>
                  </v-row>
            </v-container> 
          </div>     
      </section>

      <section id="works"> 
          <v-container>
            
            <v-row justify="center">
              <v-col cols="12" md="11" class="worksColor" align="center"> 
                <h2> Some of my works </h2>
                <v-divider> </v-divider>

                <v-row class="pt-6"> 
                  
                  <v-col cols="12" md="6"> 
                    <v-hover v-slot="{ hover }">
                      <v-img
                        :src="gallery[0].source"
                        :lazy-src="gallery[0].source"
                        aspect-ratio="2"
                      > 
                        <v-expand-transition>
                          <div
                            v-if="hover"
                            class="d-flex transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-1 white--text"
                            style="height: 100%;"
                            v-html="gallery[0].description"
                          >
                          </div>
                        </v-expand-transition>
                      </v-img>
                    </v-hover>
                  </v-col>

                  <v-col cols="12" md="6"> 
                    <v-hover v-slot="{ hover }">
                      <v-img
                        :src="gallery[1].source"
                        :lazy-src="gallery[1].source"
                        aspect-ratio="2"
                      > 
                        <v-expand-transition>
                          <div
                            v-if="hover"
                            class="d-flex transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-1 white--text"
                            style="height: 100%;"
                            v-html="gallery[1].description"
                          >
                          </div>
                        </v-expand-transition>
                      </v-img>
                    </v-hover>
                  </v-col>
                  
                  <!-- Uma coluna dividida em 2 linhas para cada imagem -->
                  <v-col cols="12" md="6"> 
                    
                    <v-row> 
                      <v-col>
                        <v-hover v-slot="{ hover }">
                          <v-img
                            :src="gallery[2].source"
                            :lazy-src="gallery[2].source"
                            aspect-ratio="2"
                          > 
                            <v-expand-transition>
                              <div
                                v-if="hover"
                                class="d-flex transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-1 white--text"
                                style="height: 100%;"
                                v-html="gallery[2].description"
                              >
                              </div>
                            </v-expand-transition>
                          </v-img>
                        </v-hover> 
                      </v-col>
                    </v-row>

                    <v-row> 
                      <v-col>
                        <v-hover v-slot="{ hover }">
                          <v-img
                            :src="gallery[4].source"
                            :lazy-src="gallery[4].source"
                            aspect-ratio="2"
                          > 
                            <v-expand-transition>
                              <div
                                v-if="hover"
                                class="d-flex transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-1 white--text"
                                style="height: 100%;"
                                v-html="gallery[4].description"
                              >
                              </div>
                            </v-expand-transition>
                          </v-img>
                        </v-hover>
                      </v-col>
                    </v-row>

                  </v-col>

                  <v-col cols="12" md="6"> 
                    <v-hover v-slot="{ hover }">
                      <v-img
                        :src="gallery[3].source"
                        :lazy-src="gallery[3].source"
                        aspect-ratio="0"
                        width="60%"
                      > 
                        <v-expand-transition>
                          <div
                            v-if="hover"
                            class="d-flex transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-3 white--text"
                            style="height: 100%;"
                            v-html="gallery[3].description"
                          > 
                          </div>
                        </v-expand-transition>
                      </v-img>
                    </v-hover>
                  </v-col>
             
                </v-row>

              </v-col>
            </v-row>
          
          </v-container>
      </section>


      <section id="contact"> 
          <v-container>          
            <v-row justify="center">
              <v-col cols="12" md="11" class="aboutMefirstColColor" align="center"> 
                <h2 class="contactTextColor"> Contact Me </h2>
                <v-divider class="dividerColorWhite"> </v-divider>

                <v-row class="pt-6"> 
                  <v-col> 
                    <ContactForm @sucess="openAlertSucess" @failure="openAlertFailure "/>
                  </v-col> 
                </v-row>

                <v-row justify="center">
                  <v-col cols="12" md="4">
                    <v-alert v-model="showAlertSucess" type="success" dismissible @input="closeSucess"> Sucess sending the email!</v-alert>
                    <v-alert v-model="showAlertFailure" type="error" dismissible @input="closeFailure"> Failed to send the email, please confirm all the fields!</v-alert>
                  </v-col>
                </v-row>
              
              </v-col>
            </v-row>
          </v-container>
      </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import ContactForm from '@/components/ContactForm.vue'

export default {
  name: 'Home',
  components : { 
    Navbar, 
    ContactForm
  }, 
  data () {
      return {
        intervalPt: {},
        intervalEn : {},
        intervalSp : {},
        intervalJava : {},
        intervalJavascript : {},
        intervalVueJs : {},
        intervalNodeJs : {},
        intervalC : {},
        intervalPython : {},
        intervalCy : {},
        intervalMongo : {},
        intervalSql : {},
        intervalReactN : {},
        valuePt: 0,
        valueEn : 0, 
        valueSp : 0, 
        valueJava : 0, 
        valueJavascript : 0,
        valueVueJs : 0,
        valueNodeJs : 0,
        valueC : 0, 
        valuePython : 0, 
        valueCy : 0, 
        valueMongo : 0, 
        valueSql : 0, 
        valueReactN : 0, 
        gallery : [
          {id : '1', description : 'Betting Spree<br>A social network dedicated to the betting enviroment, completed with a bookmaker where users could make and then share the bets that they made in groups or with friends. The shared bets could then be copied should the user want to. The bookmaker data was fetched each day from an external API through a dedicated service created to that effect.' , source : require('@/assets/1.png') },
          {id : '2', description : 'Projeto Tommi<br>A search engine interface built with the intent on easily letting users search through a large collection of documents dating to the 17th century. Multiple to query and explore the data were constructed, along with a comprehensive results page.' , source : require('@/assets/2.png') }, 
          {id : '3', description : 'Pesquisa Remédios e os seus Ingredientes<br>A search engine that was built in order to let the users search and comb through a collection of recipes dating also to the 17th century. Two main ways to query the data, either inputting recipe names or ingredient names. Along with the interface a collection of microservices were also implemented in the backend.' , source : require('@/assets/3.png') }, 
          {id : '4', description : 'Pesquisa Remédios e os seus Ingredients APP<br>A complimentary piece to the website, built using React Native. ' , source : require('@/assets/4.gif') }, 
          {id : '5', description : 'UV Forecast<br>Website that was constructed with two goals in mind, one to fetch data from an external API and show it on screen in an orderly fashing, and the other to display the results, daily, of the machine learning algorithm implemented in order to predict for each district the UV rating. A Recurrent Neural Network (LSTM) was implemented and trained in order to predict the target.' , source : require('@/assets/5.png') },
        ], 
        showAlertSucess: false, 
        showAlertFailure : false
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

      this.intervalJava = setInterval(() => {
        if (this.valueJava === 70) {
          return (this.valueJava = 70)
        }
        this.valueJava += 10
      }, 800)

      this.intervalJavascript = setInterval(() => {
        if (this.valueJavascript === 70) {
          return (this.valueJavascript = 70)
        }
        this.valueJavascript += 10
      }, 800)

      this.intervalVueJs = setInterval(() => {
        if (this.valueVueJs === 80) {
          return (this.valueVueJs = 80)
        }
        this.valueVueJs += 10
      }, 800)

      this.intervalNodeJs = setInterval(() => {
        if (this.valueNodeJs === 70) {
          return (this.valueNodeJs = 70)
        }
        this.valueNodeJs += 10
      }, 800)

      this.intervalC = setInterval(() => {
        if (this.valueC === 50) {
          return (this.valueC = 50)
        }
        this.valueC += 10
      }, 800)

      this.intervalPython = setInterval(() => {
        if (this.valuePython === 70) {
          return (this.valuePython = 70)
        }
        this.valuePython += 10
      }, 800)

      this.intervalCy = setInterval(() => {
        if (this.valueCy === 70) {
          return (this.valueCy = 70)
        }
        this.valueCy += 10
      }, 800)

      this.intervalMongo = setInterval(() => {
        if (this.valueMongo === 70) {
          return (this.valueMongo = 70)
        }
        this.valueMongo += 10
      }, 800)

      this.intervalSql = setInterval(() => {
        if (this.valueSql === 60) {
          return (this.valueSql = 60)
        }
        this.valueSql += 10
      }, 800)

      this.intervalReactN = setInterval(() => {
        if (this.valueReactN === 60) {
          return (this.valueReactN = 60)
        }
        this.valueReactN += 10
      }, 800)

    }, 

    methods : { 
        openAlertSucess() { 
          console.log("RECEBI EVENTO DE SUCESSO")
          this.showAlertSucess = true
        }, 
        openAlertFailure() { 
          console.log("RECEBI EVENTO DE INSUCESSO")
          this.showAlertFailure = true         
        },
        closeSucess() { 
          console.log("FECHEI ALERT SUCESSO")
          this.showAlertSucess = false
        }, 
        closeFailure() { 
          console.log("FECHEI ALERT FAILURE")
          this.showAlertFailure = false
        }
    }
}
</script> 


<style scoped>

.aboutMefirstColColor { 
  background-color: #3c3c3c;
}

.hoverTransitionColor { 
  background-color: #3c3c3c;
}

.aboutMesecondColColor { 
  background-color: #d8d8d8;
} 

.worksColor { 
  background-color: #d3d2d2;  
}

.alertColor { 
  background-color: #2fd80d;  
}

.aboutMeTextColor { 
  color : white
}

.contactTextColor { 
  color : white
}

.dividerColorWhite {
    border-color: rgb(255, 252, 252) !important; 
}

.dividerColorBlack {
    border-color: rgb(0, 0, 0) !important; 
}

</style>

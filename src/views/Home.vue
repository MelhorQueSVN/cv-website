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
                    Thank you<br>
                  </span>
                  
                  <div class="pt-3">        
                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-0': 'display-1']"
                      class="font-weight-light"
                    >
                      You can download the full curriculum <br>
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
import SideBar from '@/components/sidebar/SideBar.vue'
import MainBar from '@/components/mainbar/MainBar.vue'
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
        showAlertFailure : false, 
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
          this.showAlertSucess = true
        }, 
        openAlertFailure() { 
          this.showAlertFailure = true         
        },
        closeSucess() { 
          this.showAlertSucess = false
        }, 
        closeFailure() { 
          this.showAlertFailure = false
        }
    }
}
</script> 


<style scoped src="@/assets/styles/styles.css">
</style>

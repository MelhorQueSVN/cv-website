<template>
  
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
</template>

<script>
export default {
    data() { 
        return {
            gallery : [
                {
                    id : '1', 
                    description : 'Betting Spree<br>A social network dedicated to the betting enviroment, completed with a bookmaker where users could make and then share the bets that they made in groups or with friends. The shared bets could then be copied should the user want to. The bookmaker data was fetched each day from an external API through a dedicated service created to that effect.', 
                    source : require('@/assets/pictures/1.png') 
                },
                {
                    id : '2', 
                    description : 'Projeto Tommi<br>A search engine interface built with the intent on easily letting users search through a large collection of documents dating to the 17th century. Multiple to query and explore the data were constructed, along with a comprehensive results page.', 
                    source : require('@/assets/pictures/2.png') 
                }, 
                {
                    id : '3', 
                    description : 'Pesquisa Remédios e os seus Ingredientes<br>A search engine that was built in order to let the users search and comb through a collection of recipes dating also to the 17th century. Two main ways to query the data, either inputting recipe names or ingredient names. Along with the interface a collection of microservices were also implemented in the backend.', 
                    source : require('@/assets/pictures/3_gif.gif') 
                }, 
                {
                    id : '4', 
                    description : 'Pesquisa Remédios e os seus Ingredients APP<br>A complimentary piece to the website, built using React Native. ', 
                    source : require('@/assets/pictures/4.gif') 
                }, 
                {
                    id : '5', 
                    description : 'UV Forecast<br>Website that was constructed with two goals in mind, one to fetch data from an external API and show it on screen in an orderly fashing, and the other to display the results, daily, of the machine learning algorithm implemented in order to predict for each district the UV rating. A Recurrent Neural Network (LSTM) was implemented and trained in order to predict the target.', 
                    source : require('@/assets/pictures/5.png') 
                },
            ],             
        }
    }
}
</script>

<style scoped src="@/assets/styles/styles.css">
</style>

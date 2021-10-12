<template>
  
  <v-col cols="12" md="11" class="worksColor" align="center"> 
    
    <h2> {{ $t('works.title') }} </h2>
    <v-divider> </v-divider>
    
    <div v-if="$vuetify.breakpoint.smAndDown"> 
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
                  class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal white--text"
                  style="height: 100%;cursor: pointer;"
                  v-html="translatedDescription(gallery[0].id)"
                  onclick="window.open('https://github.com/CC-CloudCode', '_blank').focus()"
                >
                </div>
              </v-expand-transition>
              
              <template v-slot:placeholder>
                <v-row
                  class="fill-height ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>
            
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
                  class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal white--text"
                  style="height: 100%;cursor: pointer;"
                  v-html="translatedDescription(gallery[1].id)"
                  onclick="window.open('https://github.com/MelhorQueSVN/TommiAnalise', '_blank').focus()"
                >
                </div>
              </v-expand-transition>

              <template v-slot:placeholder>
                <v-row
                  class="fill-height ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>

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
                      class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal white--text"
                      style="height: 100%;cursor: pointer;"
                      v-html="translatedDescription(gallery[2].id)"
                      onclick="window.open('https://github.com/MelhorQueSVN/Tese-WEB-APP', '_blank').focus()"
                    >
                    </div>
                  </v-expand-transition>

                  <template v-slot:placeholder>
                    <v-row
                      class="fill-height ma-0"
                      align="center"
                      justify="center"
                    >
                      <v-progress-circular
                        indeterminate
                        color="grey lighten-5"
                      ></v-progress-circular>
                    </v-row>
                  </template>

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
                      class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal white--text"
                      style="height: 100%;cursor: pointer;"
                      v-html="translatedDescription(gallery[4].id)"
                      onclick="window.open('https://github.com/MelhorQueSVN/SA-TP2', '_blank').focus()"
                    >
                    </div>
                  </v-expand-transition>

                  <template v-slot:placeholder>
                    <v-row
                      class="fill-height ma-0"
                      align="center"
                      justify="center"
                    >
                      <v-progress-circular
                        indeterminate
                        color="grey lighten-5"
                      ></v-progress-circular>
                    </v-row>
                  </template>

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
                  class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal white--text"
                  style="height: 100%;cursor: pointer;"
                  v-html="translatedDescription(gallery[3].id)"
                  onclick="window.open('https://github.com/MelhorQueSVN/Tese-Mobile-App', '_blank').focus()"
                > 
                </div>
              </v-expand-transition>

              <template v-slot:placeholder>
                <v-row
                  class="fill-height ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>

            </v-img>
          </v-hover>
        </v-col>
  
      </v-row>
    </div>
    
    <div v-else>
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
                  class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-1 white--text"
                  style="height: 100%;cursor: pointer;"
                  v-html="translatedDescription(gallery[0].id)"
                  onclick="window.open('https://github.com/CC-CloudCode', '_blank').focus()"
                >
                </div>
              </v-expand-transition>
              
              <template v-slot:placeholder>
                <v-row
                  class="fill-height ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>
            
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
                  class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-1 white--text"
                  style="height: 100%;cursor: pointer;"
                  v-html="translatedDescription(gallery[1].id)"
                  onclick="window.open('https://github.com/MelhorQueSVN/TommiAnalise', '_blank').focus()"
                >
                </div>
              </v-expand-transition>

              <template v-slot:placeholder>
                <v-row
                  class="fill-height ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>

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
                      class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-1 white--text"
                      style="height: 100%;cursor: pointer;"
                      v-html="translatedDescription(gallery[2].id)"
                      onclick="window.open('https://github.com/MelhorQueSVN/Tese-WEB-APP', '_blank').focus()"
                    >
                    </div>
                  </v-expand-transition>

                  <template v-slot:placeholder>
                    <v-row
                      class="fill-height ma-0"
                      align="center"
                      justify="center"
                    >
                      <v-progress-circular
                        indeterminate
                        color="grey lighten-5"
                      ></v-progress-circular>
                    </v-row>
                  </template>

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
                      class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-1 white--text"
                      style="height: 100%;cursor: pointer;"
                      v-html="translatedDescription(gallery[4].id)"
                      onclick="window.open('https://github.com/MelhorQueSVN/SA-TP2', '_blank').focus()"
                    >
                    </div>
                  </v-expand-transition>

                  <template v-slot:placeholder>
                    <v-row
                      class="fill-height ma-0"
                      align="center"
                      justify="center"
                    >
                      <v-progress-circular
                        indeterminate
                        color="grey lighten-5"
                      ></v-progress-circular>
                    </v-row>
                  </template>

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
                  class="transition-fast-in-fast-out hoverTransitionColor darken-2 v-card--reveal display-3 white--text"
                  style="height: 100%;cursor: pointer;"
                  v-html="translatedDescription(gallery[3].id)"
                  onclick="window.open('https://github.com/MelhorQueSVN/Tese-Mobile-App', '_blank').focus()"
                > 
                </div>
              </v-expand-transition>

              <template v-slot:placeholder>
                <v-row
                  class="fill-height ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>

            </v-img>
          </v-hover>
        </v-col>
  
      </v-row>
    </div>
  </v-col>
</template>

<script>
export default {
    data() { 
        return {
            gallery : [
                {
                    id : '1', 
                    source : require('@/assets/pictures/1.png') 
                },
                {
                    id : '2', 
                    source : require('@/assets/pictures/2.png') 
                }, 
                {
                    id : '3', 
                    source : require('@/assets/pictures/3_gif.gif') 
                }, 
                {
                    id : '4', 
                    source : require('@/assets/pictures/4.gif') 
                }, 
                {
                    id : '5', 
                    source : require('@/assets/pictures/5.png') 
                },
            ],             
        }
    },  

    methods : { 
      translatedDescription : function(id) { 
        return this.$i18n.t('works.img-' + id + '-desc')
      }
    }

}
</script>

<style scoped src="@/assets/styles/styles.css">
</style>

<template>
  
  <v-col cols="12" md="11" class="worksColor" align="center"> 
    
    <h2> {{ $t('works.title') }} </h2>
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
                    description : this.$i18n.t('works.img-1-desc'), 
                    source : require('@/assets/pictures/1.png') 
                },
                {
                    id : '2', 
                    description : this.$i18n.t('works.img-2-desc'), 
                    source : require('@/assets/pictures/2.png') 
                }, 
                {
                    id : '3', 
                    description : this.$i18n.t('works.img-3-desc'), 
                    source : require('@/assets/pictures/3_gif.gif') 
                }, 
                {
                    id : '4', 
                    description : this.$i18n.t('works.img-4-desc'), 
                    source : require('@/assets/pictures/4.gif') 
                }, 
                {
                    id : '5', 
                    description : this.$i18n.t('works.img-5-desc'), 
                    source : require('@/assets/pictures/5.png') 
                },
            ],             
        }
    }
}
</script>

<style scoped src="@/assets/styles/styles.css">
</style>

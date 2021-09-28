<template>
    <div>   

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
              <p class="aboutMeTextColor pt-2"> {{ $t('aboutme.sidebar.languages.pt') }} </p>
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
              <p class="aboutMeTextColor pt-2"> {{ $t('aboutme.sidebar.languages.en') }} </p>
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
              <p class="aboutMeTextColor pt-2"> {{ $t('aboutme.sidebar.languages.sp') }} </p>
            </v-col>
          
          </v-row>
    
    </div>  
</template>

<script>

export default {
    data() { 
        return { 
            intervalPt: {},
            intervalEn : {},
            intervalSp : {}, 
            valuePt: 0,
            valueEn : 0, 
            valueSp : 0
        }
    }, 
    
    mounted() { 
        
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
    
    }
}
</script>


<style scoped src="@/assets/styles/styles.css">
</style>
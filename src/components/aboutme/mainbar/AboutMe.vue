<template>
    <div>
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
    </div>
</template>

<script>

export default {

}
</script>

<style scoped src="@/assets/styles/styles.css">
</style>
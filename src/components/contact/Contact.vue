<template>
  <v-col cols="12" md="11" class="aboutMefirstColColor" align="center"> 
    
    <h2 class="contactTextColor"> {{ $t('contact.title') }} </h2>
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
</template>

<script>
import ContactForm from '@/components/contact/ContactForm.vue'

export default {

    components : { 
        ContactForm
    },

    data() {
        return {
            showAlertSucess: false, 
            showAlertFailure : false, 
        }
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
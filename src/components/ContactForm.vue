<template>
    <v-form v-model="allFieldsValid">
        <v-container >
            <v-row justify="center">
                <v-col cols="12" md="4" class="backColor">
                    <v-text-field label="Name" v-model="name" clearable :rules="rules_name"> </v-text-field>
                </v-col>
            </v-row>
            <v-row justify="center" class="pt-0">
                <v-col cols="12" md="4" class="backColor">
                    <v-text-field label="Email" v-model="email" clearable :rules="rules_email" > </v-text-field>
                </v-col>
            </v-row>
            <v-row justify="center" class="pt-0">
                <v-col cols="12" md="4" class="backColor">
                    <v-textarea clearable rows="4" clear-icon="mdi-close-circle" label="Text" v-model="message" :rules="rules_message"></v-textarea>
                </v-col>
            </v-row>
            <v-row justify="center" class="pt-0">
                <v-col class="backColor" cols="12" md="4">
                    <v-btn :disabled="!allFieldsValid" text @click="sendEmail()">Submit</v-btn>
                </v-col>
            </v-row>
        </v-container>
    </v-form>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
    
    data() { 
        return { 
            allFieldsValid : false, 
            name : "", 
            rules_name : [v => !!v || 'This field is required'],
            email : "",
            rules_email : [
                e => !!e || 'This field is required', 
                e => /.+@.+/.test(e) || 'Please enter a valid email address'
            ],
            message : "",
            rules_message : [ 
                m => !!m || 'This field is required'
            ] 
        }
    },

    methods: {
        
        clearFields() {
            this.name = ""
            this.email = ""
            this.message = ""
        },
        
        sendEmail() {
            if (this.name != "" && this.email != "" && this.message != "") { 
                
                var sending_obj = { 
                    name : this.name, 
                    email : this.email, 
                    message : this.message
                }
                
                console.log(sending_obj)

                emailjs.send('service_zpxgroy', 'template_eowz1sk', sending_obj, 'user_8KuK9O7aoVlZSH91KyasI')
                    .then(function(response) {
                        console.log('SUCCESS!', response.status, response.text);
                    }, function(error) {
                        console.log('FAILED...', error);
                    });
            

                this.$emit('sucess', true)

                this.clearFields()
            
            } else { 
            
                this.$emit('failure', true)
            
            }
        }
    }
}
</script>

<style scoped>

.backColor { 
  background-color: #d8d8d8;
} 

</style>
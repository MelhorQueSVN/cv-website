<template>
    <v-form v-model="allFieldsValid">
        <v-container >
            <v-row justify="center">
                <v-col cols="12" md="4" class="contactBackColor">
                    <v-text-field :label="$t('contact.form.name')" v-model="name" clearable :rules="rules_name"> </v-text-field>
                </v-col>
            </v-row>
            <v-row justify="center" class="pt-0">
                <v-col cols="12" md="4" class="contactBackColor">
                    <v-text-field :label="$t('contact.form.email')" v-model="email" clearable :rules="rules_email" > </v-text-field>
                </v-col>
            </v-row>
            <v-row justify="center" class="pt-0">
                <v-col cols="12" md="4" class="contactBackColor">
                    <v-textarea clearable rows="4" clear-icon="mdi-close-circle" :label="$t('contact.form.text')" v-model="message" :rules="rules_message"></v-textarea>
                </v-col>
            </v-row>
            <v-row justify="center" class="pt-0">
                <v-col class="contactBackColor" cols="12" md="4">
                    <v-btn :disabled="!allFieldsValid" text @click="sendEmail()"> {{ $t('contact.form.submit') }} </v-btn>
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
            rules_name : [v => !!v || this.$i18n.t('contact.form.rule-name') ],
            email : "",
            rules_email : [
                e => !!e || this.$i18n.t('contact.form.rule-email-empty'), 
                e => /.+@.+/.test(e) || this.$i18n.t('contact.form.rule-email-invalid')
            ],
            message : "",
            rules_message : [ 
                m => !!m || this.$i18n.t('contact.form.rule-message-text')
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

<style scoped src="@/assets/styles/styles.css">
</style>
<template>
    <v-container >
        <v-row justify="center">
            <v-col cols="12" md="4" class="backColor">
                <v-text-field label="Name" v-model="name" clearable> </v-text-field>
            </v-col>
        </v-row>
        <v-row justify="center">
            <v-col cols="12" md="4" class="backColor">
                <v-text-field label="Email" v-model="email" clearable> </v-text-field>
            </v-col>
        </v-row>
        <v-row justify="center">
            <v-col cols="12" md="4" class="backColor">
                <v-textarea clearable clear-icon="mdi-close-circle" label="Text" v-model="message"></v-textarea>
            </v-col>
        </v-row>
        <v-row justify="center">
            <v-col class="backColor" cols="12" md="4">
                <v-btn text @click="sendEmail()">Submit</v-btn>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
//import emailjs from 'emailjs-com';

export default {
    
    data() { 
        return { 
            name : "", 
            email : "",
            message : "", 
        }
    },

    methods: {
        
        clearFields() {
            this.name = ""
            this.email = ""
            this.message = ""
        },
        
        sendEmail() {
            
            var sending_obj = { 
                name : this.name, 
                email : this.email, 
                message : this.message
            }
            console.log(sending_obj)
            
            /*
            emailjs.send('service_zpxgroy', 'template_eowz1sk', sending_obj, 'user_8KuK9O7aoVlZSH91KyasI')
                .then(function(response) {
                    console.log('SUCCESS!', response.status, response.text);
                }, function(error) {
                    console.log('FAILED...', error);
                });
            */

            this.$emit('sucess', true)

            this.clearFields()
        }
    }
}
</script>

<style scoped>

.backColor { 
  background-color: #d8d8d8;
} 

</style>
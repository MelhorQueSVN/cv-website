<template>

                <v-row> 
                    <!-- 11 cols dedicadas para os 4 principais e 1 para a escolha da linguagem -->
                    <v-col cols="12"  align="center" justify="center"> 

                        <v-btn text @click="$vuetify.goTo('#about-me')"> {{ $t('navbar.about') }} </v-btn>

                        <v-btn text @click="$vuetify.goTo('#works')"> {{ $t('navbar.works') }} </v-btn>

                        <v-btn text @click="$vuetify.goTo('#contact')"> {{ $t('navbar.contact') }} </v-btn>

                        <v-btn text @click="$vuetify.goTo('#ending')"> {{ $t('navbar.ending') }} </v-btn>

                        <v-menu>
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn text v-bind="attrs" v-on="on"> {{ $t('navbar.language') }} </v-btn>
                            </template>
                            <v-list>
                                <v-list-item v-for="(language,index) in list_languages" :key="index">
                                    <v-list-item-title>
                                        <v-btn text @click="changeLanguage(language.title)">
                                            {{language.title}}
                                        </v-btn>
                                    </v-list-item-title>
                                </v-list-item>
                            </v-list>
                        </v-menu>

                    </v-col>
                    
                </v-row>

</template>

<script>
export default {
    data() { 
        return { 
            list_languages : [
                { title : 'English'}, 
                { title : 'Português'}
            ]
        }
    }, 
    methods : { 
        
        changeLanguage(title) {
            let locale = ""
            if(title == "English"){ 
                locale = 'en'
                
                this.$i18n.locale = locale
                this.$router.push({
                    params: { lang: locale }
                })
            } else { 
                locale = 'pt'
                
                this.$i18n.locale = locale
                this.$router.push({
                    params: { lang: locale }
                })
            }
        }
    }
}
</script>

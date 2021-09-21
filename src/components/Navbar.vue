<template>

                <v-row> 
                    <!-- 11 cols dedicadas para os 4 principais e 1 para a escolha da linguagem -->
                    <v-col cols="12"  align="center" justify="center"> 
                        <v-btn text> Home </v-btn>

                        <v-btn text> About </v-btn>

                        <v-btn text> Resume </v-btn>

                        <v-btn text> Contact </v-btn>

                        <v-menu>
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn text v-bind="attrs" v-on="on"> Language </v-btn>
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
            console.log("Change to: " + title)
        }
    }
}
</script>

<template>
    <nav>
        <v-toolbar dense flat transparent app> 
            <v-container>
                <v-row> 
                    <!-- 11 cols dedicadas para os 4 principais e 1 para a escolha da linguagem -->
                    <v-col cols="11" align="center" justify="center"> 
                        <v-btn text> Home </v-btn>

                        <v-btn text> About </v-btn>

                        <v-btn text> Resume </v-btn>

                        <v-btn text> Contact </v-btn>
                    </v-col>
                    
                    <v-col cols="1" justify="end"> 
                        <v-btn text> Language </v-btn>
                    </v-col>
                </v-row>

            </v-container>
        </v-toolbar>
    </nav>
</template>

<script>
export default {

}
</script>

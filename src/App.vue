<template>
  
  <v-app>
    <v-content> 
      <router-view />
    </v-content>
  </v-app>
</template>

<script>


export default {
  name: 'App',

  components: {
   
  },
};
</script>


<style>
#app {
  background: url('https://user-images.githubusercontent.com/36746608/134700795-8d8fc46e-2785-49aa-95d7-fa4f8d9a97f9.jpg')
    no-repeat center center fixed !important;
  background-size: cover;
}
</style>
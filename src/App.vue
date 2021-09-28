<template>
  
  <v-app>
    <v-main> 
      <router-view />
    </v-main>
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
  background: url('assets/pictures/back.jpg')
    no-repeat center center fixed !important;
  background-size: cover;
}
</style>
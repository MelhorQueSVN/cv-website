<template>
  
  <v-app>
    <v-main> 
      <router-view />
    </v-main>
    <div class="text-center" id="footer" style="cursor: pointer;" onclick="window.open('https://github.com/MelhorQueSVN/cv-website', '_blank').focus()"> 
      {{ $t('footer.text') }}
    </div>
  </v-app>
</template>

<script>


export default {
  name: 'App',

  components: {
   
  },
};
</script>


<style scoped src="@/assets/styles/styles.css">
</style>
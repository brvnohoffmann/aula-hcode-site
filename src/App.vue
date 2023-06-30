<template>
  <div id="app">
    <BudeHeader v-on:select-champ="changeChamp" 
                v-on:change-component="changeComponent"
    />

    <BudeSection v-bind:champ="champ" 
                 v-bind:current-component="currentSectionComponent"/>
    
    <BudeFooter />

    
  </div>
</template>

<script>
import BudeHeader from './components/BudeHeader.vue'
import BudeFooter from './components/BudeFooter.vue'
import BudeSection from './components/BudeSection.vue';

export default {
  name: 'App',
  components: {
    BudeHeader,
    BudeFooter,
    BudeSection
  },
  data() {
    return {
      champ: 'Campeonato Brasileiro',
      currentSectionComponent: 'BudeSectionBanner'
    }
  },
  methods: {
    changeChamp(value){
      this.champ = value
    },

    changeComponent(value){

      let component;

      switch(value){
        case 'home':
        default:
          component = 'BudeSectionBanner'
          break;

        case 'news':
          component = 'BudeSectionNews'
          break;
      }

      this.currentSectionComponent = component
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Rajdhani&display=swap');


</style>

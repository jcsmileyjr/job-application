<template>
  <div id="app" class="background">    
    <Nav v-bind:section="this.currentView" v-bind:completed="this.pages" />
    <b-container class="center-form">
      <b-row v-if="currentView ==='personal'">
        <Personal @update:personal-info="updatePersonal" />  
      </b-row>
      <b-row v-if="currentView ==='work'"><Work @update:work-info="updateWork" /></b-row>
      <b-row v-if="currentView ==='skills'"><Skills @update:skills-info="updateSkills" /></b-row>
      <b-row v-if="currentView ==='results'">
        <Results :personal = "this.peronalData" :skills = "this.skillsData" :work ="this.workData" /></b-row>
    </b-container>    
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue';
import Personal from '@/components/Personal.vue';
import Work from '@/components/Work.vue';
import Skills from '@/components/Skills.vue';
import Results from '@/components/Results.vue';

export default {
  name: 'app',
  components: {
    Nav,
    Personal,
    Work,
    Skills,
    Results,
  },
  data(){
    return{
      peronalData:{},
      workData:{},
      skillsData:{},
      currentView:"personal",
      pages:1,
    }
  },
  methods:{
    updatePersonal(data){
      this.peronalData = data;
      this.currentView = "work";
      this.pages = 2;
    },

    updateWork(data){
      this.workData = data;
      this.currentView = "skills";
      this.pages = 3;
    },

    updateSkills(data){
      this.skillsData = data;
      this.currentView = "results";
      this.pages = 4;
    }    
  }
}
</script>

<style>
  .background {
    background-color: grey;
  }

  @media only screen and (max-width: 550px) {
    .background {
        background-color:white;
    }
  }

  .center-form {
    display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
  }
</style>

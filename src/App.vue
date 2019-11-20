<template>
  <div id="app" class="background">    
    <Nav />
    <b-container class="center-form">
      <b-row v-if="currentView ==='personal'">
        <Personal @update:personal-info="updatePersonal" />  
      </b-row>
      <b-row v-if="currentView ==='work'"><Work @update:work-info="updateWork" /></b-row>
    </b-container>    
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue';
import Personal from '@/components/Personal.vue';
import Work from '@/components/Work.vue';

export default {
  name: 'app',
  components: {
    Nav,
    Personal,
    Work,
  },
  data(){
    return{
      peronalData:{},
      workData:{},
      currentView:"work",
    }
  },
  methods:{
    updatePersonal(data){
      this.peronalData = data;
    },

    updateWork(data){
      this.workData = data;
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

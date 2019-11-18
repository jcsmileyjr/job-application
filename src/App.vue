<template>
  <div id="app">    
    <Nav />
    <b-container>
      <Personal @update:personal-info="updatePersonal" />
    </b-container>    
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue';
import Personal from '@/components/Personal.vue';

export default {
  name: 'app',
  components: {
    Nav,
    Personal,
  },
  data(){
    return{
      peronalData:{},
    }
  },
  methods:{
    updatePersonal(data){
      this.peronalData = data;
    }
  }
}
</script>

<style>
  
</style>

<template>
  <div id="app" class="background">    
    <Nav />
    <b-container >
      <b-row>
        <Personal @update:personal-info="updatePersonal" />
      </b-row>
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
  .background {
    background-color: grey;
  }
</style>

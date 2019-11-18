<template>
  <div id="app">
    <Nav />
    <Content />
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue';
import Content from '@/components/Content.vue';

export default {
  name: 'app',
  components: {
    Nav,
    Content,
  }
}
</script>

<style>
  
</style>

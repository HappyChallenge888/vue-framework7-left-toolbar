<template>
  <f7-page>

  <!-- Navigation -->
    <f7-navbar sliding class="my-tool-bar">
      <f7-nav-left>
        <f7-link icon-f7="icon-bars" panel-open="left"></f7-link>
      </f7-nav-left>
      <f7-nav-title>
        Home
      </f7-nav-title>
    </f7-navbar>

  <!-- Main Content --> 
    <f7-tabs>
      <f7-tab id="home1" tab-active>
        <Home1 />
      </f7-tab>
      <f7-tab id="home2">
        <Home2 />
      </f7-tab>
      <f7-tab id="home3">
        <Home3 />
      </f7-tab>
    </f7-tabs>

  <!-- TOOL BAR -->
    <f7-toolbar bottom-md :labels="isiOS" class="my-tool-bar">
      <f7-link tab-link="#home1" active>
        <f7-icon f7="home"></f7-icon>
      </f7-link>
      
      <f7-link tab-link="#home2">
        <f7-icon f7="search"></f7-icon>
      </f7-link>

      <f7-link tab-link="#home3">
        <f7-icon f7="camera"></f7-icon>
      </f7-link>
    </f7-toolbar>

  </f7-page>
</template>


<script>
import Home1 from './home/Home1'
import Home2 from './home/Home2'
import Home3 from './home/Home3'

export default {
  name: 'Home',
  data() {
    return {
      title: 'Hello World'
    };
  },
  computed: {
    isiOS() {
      return this.$theme.ios;
    },
    isMaterial() {
      return this.$theme.material;
    }
  },
  components: {
    Home1,
    Home2,
    Home3,
  }
};
</script>

<style scoped>
.my-tool-bar {
  background-color: red !important;
}
</style>

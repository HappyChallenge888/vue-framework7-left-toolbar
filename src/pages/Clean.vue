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
      <f7-tab id="clean_list" tab-active>
        <CleanList />
      </f7-tab>
      <f7-tab id="clean_add">
        <CleanAdd />
      </f7-tab>
      <f7-tab id="clean_my">
        <CleanMy />
      </f7-tab>
    </f7-tabs>

  <!-- TOOL BAR -->
    <f7-toolbar bottom-md :labels="isiOS" class="my-tool-bar">
      <f7-link tab-link="#clean_list" active>
        <f7-icon f7="home"></f7-icon>
      </f7-link>
      
      <f7-link tab-link="#clean_add">
        <f7-icon f7="search"></f7-icon>
      </f7-link>

      <f7-link tab-link="#clean_my">
        <f7-icon f7="camera"></f7-icon>
      </f7-link>
    </f7-toolbar>

  </f7-page>
</template>


<script>
import CleanList from './home/CleanList'
import CleanAdd from './home/CleanAdd'
import CleanMy from './home/CleanMy'

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
    CleanList,
    CleanAdd,
    myClean,
  }
};
</script>

<style scoped>
.my-tool-bar {
  background-color: red !important;
}
</style>

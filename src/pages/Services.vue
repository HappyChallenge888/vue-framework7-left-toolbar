<template>
  <f7-page>

  <!-- Navigation -->
    <f7-navbar sliding>
      <f7-nav-left>
        <f7-link icon-f7="icon-bars" panel-open="left"></f7-link>
      </f7-nav-left>
      <f7-nav-title>
        Service
      </f7-nav-title>
    </f7-navbar>

  <!-- Main Content --> 
    <f7-tabs>
      <f7-tab id="service1" tab-active>
        <Service3 />
      </f7-tab>
      <f7-tab id="service2">
        <Service2 />
      </f7-tab>
      <f7-tab id="service3">
        <Service3 />
      </f7-tab>
    </f7-tabs>

  <!-- TOOL BAR -->
    <f7-toolbar bottom-md bottom-ios :labels="isiOS">
      <f7-link :icon-f7="isiOS ? 'home' : ''" tab-link="#service3" active>
        <f7-icon f7="home"></f7-icon>
      </f7-link>
      
      <f7-link :icon-f7="isiOS ? 'home' : ''" tab-link="#service2">
        <f7-icon f7="search"></f7-icon>
      </f7-link>

      <f7-link :icon-f7="isiOS ? 'home' : ''" tab-link="#service3">
        <f7-icon f7="camera"></f7-icon>
      </f7-link>
    </f7-toolbar>

  </f7-page>
</template>


<script>
import Service1 from './service/Service1'
import Service2 from './service/Service2'
import Service3 from './service/Service3'

export default {
  name: 'Service',
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
    Service1,
    Service2,
    Service3,
  }
};
</script>

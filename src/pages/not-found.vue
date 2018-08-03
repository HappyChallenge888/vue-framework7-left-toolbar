<template>
  <f7-page>
    <f7-navbar title="Not found" back-link="Back"></f7-navbar>
    <f7-block strong>
      <p>Sorry</p>
      <p>Requested content not found.</p>
      <img :src="images.notFound" width="90%" alt="">
    </f7-block>

    <f7-list>
      <f7-list-item link="/" 
          title="Home"
          link-view="#main-view"></f7-list-item>
    </f7-list>

  </f7-page>
</template>
<script>
export default {
    data(){
        return {
           images: {
               notFound: require('../assets/images/Not-Found-Icon.png')
           } 
        }
    }
};
</script>

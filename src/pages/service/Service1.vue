<template>
  <f7-page>
    <f7-block-title> Block - {{ title }}</f7-block-title>
    <f7-block inner>
      <h6>Service 1</h6>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit.
      Distinctio est aliquam officiis quaerat placeat, cum explicabo magni
      soluta totam maxime autem minima accusamus eos suscipit dignissimos
      corporis modi voluptatum fugiat!

      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil magnam fuga error eligendi odit, dignissimos in deleniti officia cupiditate quas incidunt, aspernatur nulla debitis mollitia optio sunt aut, excepturi totam.</p>
    </f7-block>
  </f7-page>
</template>


<script>
export default {
  name: 'Service',
  data() {
    return {
      title: 'Service 1'
    };
  }
};
</script>
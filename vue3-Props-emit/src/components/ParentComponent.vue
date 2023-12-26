<template>
    <div>
      <h2>Üst Düzey Bileşen</h2>
      <p>Parent Component: {{ messageFromChild }}</p>  
      <ChildComponent :parentMessage="messageToChild" @childEvent="handleChildEvent" />
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    components: {
      ChildComponent
    },
    data() {
      return {
        messageToChild: 'Merhaba Alt Düzey!',
        messageFromChild: ''
      };
    },
    methods: {
     
      handleChildEvent(message) {
        this.messageFromChild = message;
      }
    }
  };
  </script>
  
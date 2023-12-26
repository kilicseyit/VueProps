<template>
  <div>
    <h3>Alt Düzey Bileşen</h3>
    <p>Child Component: {{ parentMessage }}</p>
    <button @click="sendMessageToParent">Üst Düzeye Mesaj Gönder</button>
  </div>
</template>

<script>
export default {
  props: {
    parentMessage: String
  },
  methods: {
    
    sendMessageToParent() {
      
      this.$emit('childEvent', 'Merhaba Üst Düzey!');
    }
  }
};
</script>

<style scoped>
</style>

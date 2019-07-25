<template>
  <button class="success" v-on:click="doneAll">All Done!</button>
</template>

<script>
export default {
  methods: {
    doneAll () {
        // Using Vuex to call action
        console.log('All done action from my component');
        this.$store.dispatch('allDone')
    }
  }
}
</script>

<style scoped>
button {
  border: 2px solid black;
  background-color: white;
  color: black;
  padding: 14px 28px;
  font-size: 16px;
  cursor: pointer;
}

/* Green */
.success {
  border-color: #4CAF50;
  color: green;
}

.success:hover {
  background-color: #4CAF50;
  color: white;
}
</style>


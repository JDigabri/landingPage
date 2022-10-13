
<template>
    <h1 id="keytitle">KEYZY</h1>
        <h1 id="title" class="centered">
        Buying software keys made
        <span class="fancy">Easy</span> .
        <form action="/" @keydown="test"></form>
        </h1>
</template>


<style scoped>

@import '../assets/main.css';

</style>

<script>
/* eslint-disable */ 
import App from "../App.vue";
export default {
    components: {
    App
  },

  methods: {
    test: function() {
            console.log(App.data().isHidden);
        }
    }
}
</script>

<template>
    <div class ="BG">
        <h1 id="title" class="centered">
        Buying software keys made
        <span class="fancy">Easy</span>
    </h1>
    <div class = "centeredBUT">
        <CButton color="light">Join Our mailing List</CButton>
        <br>
        <CButton color="light" variant="outline" class = "underbutton">See how it works</CButton>
    </div>
</div>
<br>
<br>
<br>

</template>

<script>
// https://coreui.io/vue/docs/layout/containers.html
import '@coreui/coreui/dist/css/coreui.min.css'
import { CButton } from '@coreui/vue';

export default {
    name: 'HomeView',
    components: {
        CButton,
    }
}
</script>

<style scoped>
    @import '../assets/main.css';
</style>

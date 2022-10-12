<script>
    // https://coreui.io/vue/docs/layout/containers.html
    import '@coreui/coreui/dist/css/coreui.min.css'
    import { CCard } from '@coreui/vue';
    import { CCardImage } from '@coreui/vue';
    import { CCardBody } from '@coreui/vue';
    import { CCardTitle } from '@coreui/vue';
    import { CCardText } from '@coreui/vue';
    import { CButton } from '@coreui/vue';
    export default {
        name: 'HomeView',
        components: {
            CCard,
            CCardImage,
            CCardBody,
            CCardTitle,
            CCardText,
            CButton
        }
    }
</script>


<template>
    <div class = "BG">
        <CCard style="width: 18rem; background-color: #322F37;">
        <CCardImage orientation="top" src="../images/key.png" />
            <CCardBody>
                <CCardTitle>Card title</CCardTitle>
                <CCardText>Some quick example text to build on the card title and make up the bulk of the card's content.</CCardText>
                <CButton href="#">Go somewhere</CButton>
            </CCardBody>
        </CCard>
    </div>
</template>

<script>

</script>

<style scoped>
.BG{
    margin:10px;
    background-color: #000000;
    height:75vh;

}

</style>
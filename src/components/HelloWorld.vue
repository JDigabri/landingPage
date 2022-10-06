<script>
// https://coreui.io/vue/docs/layout/containers.html
import '@coreui/coreui/dist/css/coreui.min.css'
import { CCarousel } from '@coreui/vue';
import { CCarouselItem } from '@coreui/vue';
import { CCarouselCaption } from '@coreui/vue';
export default {
    name: 'HomeView',
    components: {
        CCarousel,
        CCarouselItem,
        CCarouselCaption
    }
}
</script>

<template>
<div>
<CCarousel controls indicators>
  <CCarouselItem style="height: 91vh">
    <img class="d-block w-100" src="../images/vueOMG.jpg" alt="slide 1"/>
    <CCarouselCaption class="d-none d-md-block">
      <h5>First slide label</h5>
      <p>Some representative placeholder content for the first slide.</p>
    </CCarouselCaption>
  </CCarouselItem>
  <CCarouselItem style="height: 91vh">
    <img class="d-block w-100" src="../images/rec.png" alt="slide 2"/>
    <CCarouselCaption class="d-none d-md-block">
      <h5>First slide label</h5>
      <p>Some representative placeholder content for the first slide.</p>
    </CCarouselCaption>
  </CCarouselItem>
  <CCarouselItem style="height: 91vh">
    <img class="d-block w-100" src="../images/ang.png" alt="slide 3"/>
    <CCarouselCaption class="d-none d-md-block">
      <h5>First slide label</h5>
      <p>Some representative placeholder content for the first slide.</p>
    </CCarouselCaption>
  </CCarouselItem>
</CCarousel>
</div>
</template>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

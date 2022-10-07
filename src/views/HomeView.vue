<script>
import CardComponent from '@/components/cardComponent.vue'
import ImageComponetent from '../components/ImageComponetent.vue'
import FoooterRights from '../components/foooterRights.vue'

  
  export default {
    name: 'HomeView',
    components: {
    ImageComponetent,
    CardComponent,
    FoooterRights
}
  }
  </script>

<template>
  <div id="home">
    <ImageComponetent></ImageComponetent>
    <card-component></card-component>
    <FoooterRights></FoooterRights>
  </div>
</template>
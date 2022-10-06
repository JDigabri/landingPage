<script>
import CardComponent from '@/components/cardComponent.vue'
  // @ is an alias to /src
  
import ImageComponetent from '../components/ImageComponetent.vue'

  
  export default {
    name: 'HomeView',
    components: {
    ImageComponetent,
        CardComponent,
}
  }
  </script>

<template>
  <div class="home">
    <ImageComponetent></ImageComponetent>
    <card-component></card-component>
  </div>
</template>
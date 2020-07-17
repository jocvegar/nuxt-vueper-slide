<template>
    <vueper-slides 
        autoplay
        class="no-shadow"
        :visible-slides="3"
        slide-multiple
        :infinite="true" 
        :arrows="false"
        :bullets="false"
        :gap="1"
        progress
        :slide-ratio="1 / 3"
        :dragging-distance="70"
        :breakpoints="{ 800: { 
            visibleSlides: 1, 
            slideRatio: 1,
            } 
        }">
        <vueper-slide
            v-for="(slide, i) in slides"
            :key="i"
            :image="slide.image" />
    </vueper-slides>
  
</template>

<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'

export default {
    components: { VueperSlides, VueperSlide },
    data: () => ({
        slides: [
            { image: require('@/assets/images/image-1.jpg') },
            { image: require('@/assets/images/image-2.jpg') },
            { image: require('@/assets/images/image-3.jpg') },
            { image: require('@/assets/images/image-4.jpg') },
            { image: require('@/assets/images/image-5.jpg') },
        ]
    })
}
</script>

<style>

</style>

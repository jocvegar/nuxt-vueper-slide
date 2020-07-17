<template>
    <vueper-slides fade :touchable="false">
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
        ]
    })
}
</script>

<style>

</style>

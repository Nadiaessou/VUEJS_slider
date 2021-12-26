<template>
    <div>
        <carousel>
            <carousel-slide v-for="n in slides" :index="n - 1">
                <div class="title">Slide {{ n }}</div>
                <img v-bind:src="require('./components/carousel/image' + n +'.jpg')" class="imgslide">
            </carousel-slide>
        </carousel>
    </div>
</template>
<script>
import Carousel from './components/carousel/Carousel'
import CarouselSlide from './components/carousel/CarouselSlide'

export default {
    data () {
        return {
            slides: 5,
        }
    },
    components: {
        Carousel,
        CarouselSlide
  }
}
</script>
<style>
.imgslide {
    width: 100%;
}
.title {
    position: absolute;
    left: 0;
    right: 0;
    text-align: center;
    top: 50%;
    color: #fff;
    font-size: 16px;
}
</style>

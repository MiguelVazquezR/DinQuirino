<template>
    <swiper :modules="modules" :slides-per-view="'auto'" :space-between="20" :free-mode="true" :mousewheel="false"
        :grab-cursor="true" class="collage-swiper">
        <swiper-slide v-for="(image, index) in images" :key="index" :class="['collage-slide', `size-${image.size}`]">
            <img :src="image.src" :alt="`Image ${index + 1}`" class="selected-none" :draggable="false" />
        </swiper-slide>
    </swiper>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { FreeMode, Mousewheel } from 'swiper';
import 'swiper/css';
import 'swiper/css/free-mode';

export default {
    components: {
        Swiper,
        SwiperSlide
    },

    props: {
        images: {
            type: Array,
            required: true
        }
    },

    setup() {
        return {
            modules: [FreeMode, Mousewheel]
        };
    }
};
</script>

<style scoped>
.collage-swiper {
    width: 100%;
    padding: 5px;
}

.collage-slide {
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s;
}

.collage-slide:hover {
    transform: scale(1.03);
}

.collage-slide img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.size-small {
    width: 150px;
    height: 150px;
}

.size-medium {
    width: 200px;
    height: 250px;
}

.size-large {
    width: 300px;
    height: 200px;
}
</style>
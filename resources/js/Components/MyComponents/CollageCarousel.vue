<template>
    <swiper :modules="modules" :slides-per-view="'auto'" :space-between="20" :free-mode="true" :mousewheel="false"
        :grab-cursor="true" class="collage-swiper">
        <swiper-slide @click="openPreview(index)" v-for="(image, index) in images" :key="index" :style="{ width: image.w}"
            class="bg-[#8B5E3C44] flex justify-center rounded-2xl collage-slide transition-transform duration-300">
            <img :src="image.src" :alt="`Image ${index + 1}`" class="selected-none h-80 object-contain"
                :draggable="false" />
        </swiper-slide>
    </swiper>
    <DialogModal :show="showImageModal" @close="showImageModal = false" maxWidth="6xl">
        <template #content>
            <img :src="images[selectedImage].src" class="w-full h-auto object-contain" />
        </template>
        <template #footer>
            <button class="bg-gray-400 text-white px-4 py-2 rounded" @click="showImageModal = false">Cerrar</button>
        </template>
    </DialogModal>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { FreeMode, Mousewheel } from 'swiper';
import 'swiper/css';
import 'swiper/css/free-mode';
import DialogModal from '../DialogModal.vue';

export default {
    name: 'CollageCarousel',
    data() {
        return {
            showImageModal: false,
            selectedImage: null
        };
    },
    components: {
        Swiper,
        SwiperSlide,
        DialogModal,
    },
    props: {
        images: {
            type: Array,
            required: true
        }
    },
    methods: {
        openPreview(index) {
            this.selectedImage = index;
            this.showImageModal = true;
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

.collage-slide:hover {
    transform: scale(1.04);
}
</style>
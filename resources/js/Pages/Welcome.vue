<template>
    <LandingLayout title="Bienvenidos">
        <section>
            <figure class="w-[98%] mx-auto absolute top-3 left-4 -z-10">
                <img src="@/../../public/images/hero.png" :draggable="false" class="w-full select-none"
                    alt="Campo de maiz con tierra y cielo azul">
            </figure>
        </section>
        <section class="mt-[90vh]" id="history">
            <h1 class="text-center text-3xl">HISTORIA</h1>
        </section>
    </LandingLayout>
</template>
<script>
import LandingLayout from '@/Layouts/LandingLayout.vue';

export default {
    name: "Welcome",
    components: {
        LandingLayout,
    },
    methods: {
        
    }
}
</script>

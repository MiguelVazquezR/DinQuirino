<template>
    <div>
        <Head :title="title" />
        <nav class="flex items-center justify-between px-12 my-6">
            <ApplicationLogo class="h-14" />
            <section class="mr-10">
                <ul class="hidden lg:flex items-center space-x-14 text-xl text-white">
                    <li>
                        <button @click="scrollToElement('history')">Historia</button>
                    </li>
                    <li>
                        <button @click="scrollToElement('galery')">Galería</button>
                    </li>
                </ul>
            </section>
        </nav>
        <main>
            <slot />
        </main>
        <footer class="mt-10 bg-gradient-to-r from-[#8B5E3C] to-[#3B2311] text-white py-2 lg:py-4 px-4 lg:px-8">
            <div class="hidden lg:flex">
                <section class="items-center justify-between">
                    <ApplicationLogo color="white" class="h-14" />
                    <div>
                        <span>Hecho por </span>
                        <a href="https://dtw.com.mx" target="_blank" class="inline-block">
                            <img src="@/../../public/images/dtw.png" alt="Logo de la compañía que desarrolló la página web: DTW" class="h-12 inline-block">
                        </a>
                    </div>
                </section>
                <p class="text-center">Copyright &copy; {{ currentYear }}. Todos los derechos reservados.</p>
            </div>
            <div class="lg:hidden">
                <section>
                    <ApplicationLogo color="white" class="h-14" />
                    <p class="text-center">Copyright &copy; {{ currentYear }}. Todos los derechos reservados.</p>
                    <div class="text-end mt-3">
                        <span>Hecho por </span>
                        <a href="https://dtw.com.mx" target="_blank" class="inline-block">
                            <img src="@/../../public/images/dtw.png" alt="Logo de la compañía que desarrolló la página web: DTW" class="h-12 inline-block">
                        </a>
                    </div>
                </section>
            </div>
        </footer>
    </div>
</template>
<script>
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import { Head } from '@inertiajs/vue3';

export default {
    name: "LandingLayout",
    data() {
        return {
            currentYear: new Date().getFullYear(),
        }
    },
    components: {
        Head,
        ApplicationLogo,
    },
    props: {
        title: {
            type: String,
            default: "Bienvenidos",
        },
    },
    methods: {
        scrollToElement(id) {
            const element = document.getElementById(id);
            element.scrollIntoView({
                behavior: 'smooth'
            });
        },
    }
}
</script>
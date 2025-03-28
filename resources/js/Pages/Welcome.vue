<template>
    <LandingLayout title="Bienvenidos" class="overflow-x-hidden">
        <section>
            <figure class="w-[98%] mx-auto absolute top-3 left-4 -z-10">
                <img src="@/../../public/images/hero.png" :draggable="false" class="w-full select-none"
                    alt="Campo de maiz con tierra y cielo azul">
            </figure>
        </section>
        <section class="mt-[96vh] pt-10" id="history">
            <h1 class="text-center text-3xl">HISTORIA</h1>
            <article class="mt-5 relative">
                <div
                    class="bg-[#8B5E3C33] h-32 w-2/3 absolute top-8 left-0 intersect:motion-translate-x-in-[-90%] motion-translate-y-in-[0%] motion-duration-[2.00s]/translate">
                </div>
                <div
                    class="bg-[#8B5E3C] shadow-lg rounded-l-2xl h-72 w-1/2 absolute top-2 right-0 motion-translate-x-in-[90%] motion-translate-y-in-[0%] motion-duration-[4.00s]/translate">
                </div>
                <img src="@/../../public/images/quirino1.png" alt="Don Quirino sentado en una silla"
                    class="select-none w-[30%] absolute top-10 left-[40%] z-10 motion-preset-expand motion-duration-2000"
                    :draggable="false">
                <div
                    class="bg-[#8B5E3C] shadow-lg rounded-r-2xl h-52 w-[52%] absolute bottom-4 left-0 motion-translate-x-in-[-90%] motion-translate-y-in-[0%] motion-duration-[4.00s]/translate">
                </div>
                <div
                    class="bg-[#8B5E3C33] h-44 rounded-l-2xl w-[31%] absolute bottom-20 right-0 motion-translate-x-in-[90%] motion-translate-y-in-[0%] motion-duration-[2.00s]/translate">
                </div>
                <figure
                    class="w-[30%] relative motion-scale-in-[0.45] motion-translate-x-in-[-25%] motion-translate-y-in-[73%] motion-opacity-in-[0%] motion-rotate-in-[-15deg] motion-blur-in-[5px] motion-duration-[1.0s] motion-duration-[1.0s]/scale motion-duration-[1.0s]/translate motion-duration-[1.63s]/rotate">
                    <div class="absolute top-0 left-0 font-bold py-8 px-14 w-full">
                        <h2 class="text-2xl text-center">Don Quirino: El hombre que liberó a Tepatitlán</h2>
                        <p class="mt-6 text-xl font-thin">
                            En una época de lucha y revolución, Don Quirino, un hombre de principios y valentía, marcó
                            la historia de Tepatitlán. <br><br>
                            Nació en el año 1886, se caso con María Dolores Martin Villalobos y vivío en el corazón de
                            Jalisco.
                        </p>
                    </div>
                    <img src="@/../../public/images/history_content.png" alt="Contenedor de historia"
                        class="select-none w-full" :draggable="false">
                </figure>
            </article>
            <article class="mt-5 relative">
                <div
                    class="bg-[#8B5E3C33] h-32 w-2/3 absolute top-8 left-0 intersect:motion-translate-x-in-[-90%] motion-translate-y-in-[0%] motion-duration-[2.00s]/translate">
                </div>
                <div
                    class="bg-[#8B5E3C] shadow-lg rounded-l-2xl h-72 w-1/2 absolute top-2 right-0 motion-translate-x-in-[90%] motion-translate-y-in-[0%] motion-duration-[4.00s]/translate">
                </div>
                <img src="@/../../public/images/quirino1.png" alt="Don Quirino sentado en una silla"
                    class="select-none w-[30%] absolute top-10 left-[40%] z-10 motion-preset-expand motion-duration-2000"
                    :draggable="false">
                <div
                    class="bg-[#8B5E3C] shadow-lg rounded-r-2xl h-52 w-[52%] absolute bottom-4 left-0 motion-translate-x-in-[-90%] motion-translate-y-in-[0%] motion-duration-[4.00s]/translate">
                </div>
                <div
                    class="bg-[#8B5E3C33] h-44 rounded-l-2xl w-[31%] absolute bottom-20 right-0 motion-translate-x-in-[90%] motion-translate-y-in-[0%] motion-duration-[2.00s]/translate">
                </div>
                <figure
                    class="w-[30%] relative motion-scale-in-[0.45] motion-translate-x-in-[-25%] motion-translate-y-in-[73%] motion-opacity-in-[0%] motion-rotate-in-[-15deg] motion-blur-in-[5px] motion-duration-[1.0s] motion-duration-[1.0s]/scale motion-duration-[1.0s]/translate motion-duration-[1.63s]/rotate">
                    <div class="absolute top-0 left-0 font-bold py-8 px-14 w-full">
                        <h2 class="text-2xl text-center">Levantamiento en armas</h2>
                        <p class="mt-6 text-xl font-thin">
                            En 1914, siendo teniente coronel, se levanto en armas junto a Enrique Estrada, liderando
                            1,200 hombres saliendo de Tepatitlá rumbo a Guadalajara
                            <br><br>
                            Enfrentaron y derrotaron a las fuerzas del general Mier, uno de los más fieles a Porfirio
                            Díaz.
                            <br><br>
                            Su valentía en batalla lo convirtió en una figura clave en la Revolución
                        </p>
                    </div>
                    <img src="@/../../public/images/history_content.png" alt="Contenedor de historia"
                        class="select-none w-full" :draggable="false">
                </figure>
            </article>
        </section>
        <section class="mt-32" id="galery">
            <h1 class="text-center text-3xl">GALERÍA</h1>
            <div class="bg-[#E8DFD8] py-8 mt-3">
                <CollageCarousel :images="images" />
            </div>
        </section>
    </LandingLayout>
</template>
<script>
import CollageCarousel from '@/Components/MyComponents/CollageCarousel.vue';
import LandingLayout from '@/Layouts/LandingLayout.vue';
import galery1 from '@/../../public/images/quirino1.png';
import galery2 from '@/../../public/images/quirino1.png';
import galery3 from '@/../../public/images/quirino1.png';

export default {
    name: "Welcome",
    data() {
        return {
            images: [
                { src: galery1, size: 'small' },
                { src: galery2, size: 'small' },
                { src: galery3, size: 'small' },
                { src: galery1, size: 'small' },
                { src: galery2, size: 'medium' },
                { src: galery3, size: 'large' },
                { src: galery1, size: 'small' },
                { src: galery2, size: 'medium' },
                { src: galery3, size: 'large' },
                { src: galery1, size: 'small' },
                { src: galery2, size: 'medium' },
                { src: galery3, size: 'large' },
                { src: galery1, size: 'small' },
                { src: galery2, size: 'medium' },
                { src: galery3, size: 'large' },
                { src: galery1, size: 'small' },
                { src: galery2, size: 'medium' },
                { src: galery3, size: 'large' },
            ]
        }
    },
    components: {
        LandingLayout,
        CollageCarousel,
    },
    methods: {

    }
}
</script>

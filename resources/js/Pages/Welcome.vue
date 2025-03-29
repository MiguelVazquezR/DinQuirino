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
            <div class="flex justify-center gap-4 my-4">
                <button @click="prevSlide" :disabled="currentSlide == 1"
                    class="px-4 py-2 bg-gray-200 rounded hover:bg-gray-300 disabled:opacity-50">
                    Anterior
                </button>
                <button @click="stopAudio" class="px-4 py-2 bg-red-200 rounded hover:bg-red-300">
                    Detener
                </button>
                <button @click="nextSlide" :disabled="currentSlide == 4"
                    class="px-4 py-2 bg-gray-200 rounded hover:bg-gray-300 disabled:opacity-50">
                    Siguiente
                </button>
            </div>
            <article v-if="currentSlide == 1" class="mt-5 relative">
                <div
                    class="bg-[#8B5E3C33] h-32 w-2/3 absolute top-8 left-0 intersect:motion-translate-x-in-[-90%] motion-translate-y-in-[0%] motion-duration-[2.00s]/translate">
                </div>
                <div
                    class="bg-[#8B5E3C] shadow-lg rounded-l-2xl h-72 w-1/2 absolute top-2 right-0 motion-translate-x-in-[90%] motion-translate-y-in-[0%] motion-duration-[4.00s]/translate">
                </div>
                <img src="@/../../public/images/slide1.png" alt="Don Quirino sentado en una silla"
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
                            Nació en el año 1886, se caso con María Dolores Martin Villalobos y vivió en el corazón de
                            Jalisco.
                        </p>
                    </div>
                    <img src="@/../../public/images/history_content.png" alt="Contenedor de historia"
                        class="select-none w-full" :draggable="false">
                </figure>
            </article>
            <article v-if="currentSlide == 2" class="mt-5 relative">
                <div
                    class="bg-[#8B5E3C33] h-32 w-2/3 absolute top-8 left-0 intersect:motion-translate-x-in-[-90%] motion-translate-y-in-[0%] motion-duration-[2.00s]/translate">
                </div>
                <div
                    class="bg-[#8B5E3C] shadow-lg rounded-l-2xl h-72 w-1/2 absolute top-2 right-0 motion-translate-x-in-[90%] motion-translate-y-in-[0%] motion-duration-[4.00s]/translate">
                </div>
                <img src="@/../../public/images/slide2.png" alt="Don Quirino sentado en una silla"
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
                            En 1914, siendo teniente coronel, se levantó en armas junto a Enrique Estrada, liderando
                            1,200 hombres saliendo de Tepatitlán rumbo a Guadalajara
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
            <article v-if="currentSlide == 3" class="mt-5 relative">
                <div
                    class="bg-[#8B5E3C33] h-32 w-2/3 absolute top-8 left-0 intersect:motion-translate-x-in-[-90%] motion-translate-y-in-[0%] motion-duration-[2.00s]/translate">
                </div>
                <div
                    class="bg-[#8B5E3C] shadow-lg rounded-l-2xl h-72 w-1/2 absolute top-2 right-0 motion-translate-x-in-[90%] motion-translate-y-in-[0%] motion-duration-[4.00s]/translate">
                </div>
                <img src="@/../../public/images/slide3.png" alt="Don Quirino sentado en una silla"
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
                        <h2 class="text-2xl text-center">La huida a caballo</h2>
                        <p class="mt-6 text-xl font-thin">
                            Años después, en 1926 y 1927, fue presidende de Tepatitlán, gobernando con justicia y
                            defendiendo al pueblo de la opresión.
                            <br><br>
                            Sin embargo, su lucha le costó enemigos. Intentaron fusilarlo en varias ocasiones, víctima
                            de celos políticos.
                            <br><br>
                            En una de las más dramáticas, fue capturado y sentenciado a muerte.
                            <br><br>
                            La orden estaba dada, pero su familia suplicó que le permitieran ir a la iglesia antes de
                            ejecución.
                            En un golpe de astucia, logró escapar a caballo, dejando a sus verdugos burlados.
                        </p>
                    </div>
                    <img src="@/../../public/images/history_content.png" alt="Contenedor de historia"
                        class="select-none w-full" :draggable="false">
                </figure>
            </article>
            <article v-if="currentSlide == 4" class="mt-5 relative">
                <div
                    class="bg-[#8B5E3C33] h-32 w-2/3 absolute top-8 left-0 intersect:motion-translate-x-in-[-90%] motion-translate-y-in-[0%] motion-duration-[2.00s]/translate">
                </div>
                <div
                    class="bg-[#8B5E3C] shadow-lg rounded-l-2xl h-72 w-1/2 absolute top-2 right-0 motion-translate-x-in-[90%] motion-translate-y-in-[0%] motion-duration-[4.00s]/translate">
                </div>
                <img src="@/../../public/images/slide1.png" alt="Don Quirino sentado en una silla"
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
                        <h2 class="text-2xl text-center">Su legado y Tepatitlán</h2>
                        <p class="mt-6 text-xl font-thin">
                            Tiempo después se presentó en Guadalajara y demostró su inocencia, consolidando su lugar en
                            la historia como un líder íntegro y valiente.
                            <br><br>
                            Su legado sigue vivo, no solo en Tepatitlán sino en cada historia que lo recuerda como el
                            simbolo de honor y resistencia.
                        </p>
                    </div>
                    <img src="@/../../public/images/history_content.png" alt="Contenedor de historia"
                        class="select-none w-full" :draggable="false">
                </figure>
            </article>
            <!-- Reproductor de audio (oculto) -->
            <audio ref="audioPlayer" @ended="handleAudioEnd"></audio>
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
import galery1 from '@/../../public/images/galery/g1.png';
import galery2 from '@/../../public/images/galery/g2.png';
import galery3 from '@/../../public/images/galery/g3.png';
import galery4 from '@/../../public/images/galery/g4.png';
import galery5 from '@/../../public/images/galery/g5.png';
import galery6 from '@/../../public/images/galery/g6.png';
import galery7 from '@/../../public/images/galery/g7.png';
import galery8 from '@/../../public/images/galery/g8.png';
import slide1 from '@/../../public/audios/slide1.mp3';
import slide2 from '@/../../public/audios/slide2.mp3';
import slide3 from '@/../../public/audios/slide3.mp3';
import slide4 from '@/../../public/audios/slide4.mp3';

export default {
    name: "Welcome",
    data() {
        return {
            currentSlide: 1,
            images: [
                { src: galery1, w: '210px' },
                { src: galery2, w: '210px' },
                { src: galery3, w: '430px' },
                { src: galery4, w: '600px' },
                { src: galery5, w: '230px' },
                { src: galery6, w: '600px' },
                { src: galery7, w: '350px' },
                { src: galery8, w: '500px' },
            ],
            audios: [
                slide1,
                slide2,
                slide3,
                slide4,
            ],
        }
    },
    components: {
        LandingLayout,
        CollageCarousel,
    },
    mounted() {
        // Reproducir el audio del primer slide al cargar la página
        this.playAudio();
    },
    methods: {
        prevSlide() {
            if (this.currentSlide > 1) {
                this.currentSlide--;
                this.playAudio();
            }
        },
        nextSlide() {
            if (this.currentSlide < 4) {
                this.currentSlide++;
                this.playAudio();
            }
        },
        playAudio() {
            // Espera a que el DOM se actualice para asegurar que el reproductor está listo
            this.$nextTick(() => {
                const audioElement = this.$refs.audioPlayer;
                if (audioElement) {
                    audioElement.pause();
                    audioElement.src = this.audios[this.currentSlide - 1];
                    audioElement.play().catch(e => console.error("Error al reproducir:", e));
                }
            });
        },
        stopAudio() {
            const audioElement = this.$refs.audioPlayer;
            if (audioElement) {
                audioElement.pause();
                audioElement.currentTime = 0; // Reinicia al inicio
                this.isPlaying = false;
            }
        },
        handleAudioEnd() {
            if (this.currentSlide < this.audios.length) {
                this.nextSlide();
            }
        },
    },
    watch: {
        currentSlide() {
            this.playAudio();
        }
    }
}
</script>

<template>
    <section class="feedback mx-auto mb-36">
        <div class="dots-frame">
            <img :src="`./src/assets/images/dots-blue.png`">
        </div>
        <div class="wrapper relative mx-auto max-w-6xl">
            <div class="container flex flex-col mx-auto">
                <div class="feedback-title mb-32 mt-14">
                    <h5 class="text-xs mb-6">FEEDBACK CUSTOMER</h5>
                    <h1 class="text-5xl">Apa kata mereka tentang Bisloka ?</h1>
                </div>
                <Carousel class="feedback-item flex justify-between" :settings="settings" :breakpoints="breakpoints">
                    <Slide v-for="customer in custList" :key="customer.id">
                        <div class="p-12">
                            <div class="feedback-card rounded-xl shadow-lg mb-10 bg-white">
                            <div class="flex flex-col py-10 px-4 text-center">
                                <div class="mx-auto -mt-16">
                                    <img class="h-16" :src="customer.image">
                                </div>
                                <div class="fd-title mb-3">
                                    <h1 class="text-lg mb-1">{{customer.name}}</h1>
                                    <h2 class="text-sm">{{customer.role}}</h2>
                                </div>
                                <div class="fd-desc mx-auto">
                                    <p class="text-xs leading-loose mb-5">{{customer.review}}</p>
                                    <img class="h-5 mx-auto" :src="customer.rating">
                                </div>
                            </div>
                        </div>
                        </div>
                    </Slide>
                    <template #addons>
                        <Navigation />
                        <!-- <button type="button" @click="prev()" class="carousel__prev w-20 h-20 rounded-full bg-white shadow-lg mr-3" aria-label="Navigate to previous slide">
                            <img class="mx-auto" :src="`./src/assets/images/chevron-left.svg`">
                        </button>
                        <button type="button" @click="next()" class="carousel__next w-20 h-20 rounded-full bg-blue-300 shadow-lg mr-3" aria-label="Navigate to next slide">
                            <img class="mx-auto" :src="`./src/assets/images/chevron-right.svg`">
                        </button> -->
                    </template>
                </Carousel>
                <!-- <div class="feedback-btn-slider flex">
                </div> -->
            </div>
        </div>
    </section>
</template>

<script>
import { Carousel, Navigation, Slide } from 'vue3-carousel';

import 'vue3-carousel/dist/carousel.css';
export default {
    name: 'FeedbackSection',
    components: {
        Carousel,
        Slide,
        Navigation,
    },
    setup(){
        const custList = [
            {
                id: 1,
                name: 'Margareth Carbell',
                role: 'Product Designer, Taripedia',
                image: './src/assets/images/cust-1.png',
                review: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been. typesetting',
                rating:  './src/assets/images/star-rating.svg'
            },
            {
                id: 2,
                name: 'Sergio Mariotelli',
                role: 'Founder, Goprint',
                image: './src/assets/images/cust-2.png',
                review: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been. typesetting',
                rating:  './src/assets/images/star-rating.svg'
            },
            {
                id: 3,
                name: 'John Workson',
                role: 'College Student',
                image: './src/assets/images/cust-3.png',
                review: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been. typesetting',
                rating:  './src/assets/images/star-rating.svg'
            },
            {
                id: 4,
                name: 'John Doe',
                role: 'Hacker',
                image: './src/assets/images/cust-2.png',
                review: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been. typesetting',
                rating:  './src/assets/images/star-rating.svg'
            },
        ]
        return {custList}
    },
    data: () => ({
        // carousel settings
        settings: {
            itemsToShow: 3,
            snapAlign: 'start',
        },
        // breakpoints are mobile first
        // any settings not specified will fallback to the carousel settings
        breakpoints: {
        // 700px and up
            700: {
                itemsToShow: 3,
                snapAlign: 'start',
            },
            // 1024 and up
            1024: {
                itemsToShow: 3,
                snapAlign: 'start',
            },
        },
    })
}
</script>
<style scoped>
    .dots-frame{
        position:absolute;
        left: 8%;
        top: 26%;
    }
    .feedback{
        max-height: 830px;
        max-width:1440px;
        position: relative;
        overflow-x: hidden;
    }
    .feedback-card{
        max-width: 354px;
        width: 354px;
    }
    .fd-title h1{
        font-family: "GilroyBold";
    }
    .fd-desc{
        max-width: 95.7%; 
    }
    .feedback-title h5{
        letter-spacing: .3em;
        color: #3BC5E9;
    }
    h1{
        font-family: "AmsiProSemiBold";
    }
</style>
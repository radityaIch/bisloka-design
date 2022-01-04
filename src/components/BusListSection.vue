<template>
    <section class="bus-list mx-auto mb-36">
        <div class="wrapper relative mx-auto max-w-6xl">
            <div class="container flex flex-col mx-auto">
                <div class="bus-list-title text-center mb-14">
                    <h5 class="text-xs mb-6">ARMADA KAMI</h5>
                    <h1 class="text-5xl">Sesuaikan Dengan Keperluan Anda</h1>
                </div>
                <Carousel class="bus-list-item flex justify-between" :settings="settings" :breakpoints="breakpoints">
                    <Slide v-for="bus in busList" :key="bus.id" >
                        <div class="bus-list-card rounded-xl shadow-lg mb-10 bg-white">
                            <div class="flex flex-col p-12">
                                <div class="mx-auto mb-5">
                                    <img class="h-44" :src="bus.image">
                                </div>
                                <div class="mb-5 text-left">
                                    <span class="bg-white py-1 px-2 rounded-full shadow-lg">
                                        <img class="inline" :src="`/src/assets/images/user-icon.png`">
                                    </span>
                                    <p class="inline text-sm ml-3">{{bus.seat}} Seats</p>
                                </div>
                                <div class="text-left"><h1 class="bl-title text-xl mb-5">{{bus.name}}</h1></div>
                                <div class="text-left">
                                    <span class="text-sm"><strong>Mulai Dari : </strong></span>
                                    <strong><p class="text-blue-400 text-2xl">{{bus.price}}</p></strong>
                                </div>
                            </div>
                        </div>
                    </Slide>
                    <template #addons>
                        <Navigation />
                    </template>
                </Carousel>
            </div>
            <div class="flex justify-end">
                <button class="bus-list-btn px-16 py-4 pt-3 rounded-full mt-4">Lihat Semua Bus <span><img class="inline" :src="`./src/assets/images/arrow-icon.svg`"></span></button>
            </div>
        </div>
        <div class="dots-frame">
            <img :src="`/src/assets/images/dots-blue.png`">
        </div>
    </section>
</template>

<script>
import { Carousel, Navigation, Slide } from 'vue3-carousel';

import 'vue3-carousel/dist/carousel.css';
export default {
    name: 'BusListSection',
    components: {
        Carousel,
        Slide,
        Navigation,
    },
    setup(){
        const busList = [
            {
                id: 1,
                name: 'Jetbus 29 Seater Balideva Transport',
                seat: '30',
                image: '/src/assets/images/item-bus-1.png',
                price: 'Rp. 2.500.000'
            },
            {
                id: 2,
                name: 'Toyota Coaster Seater Travelink Trans',
                seat: '100',
                image: '/src/assets/images/item-bus-2.png',
                price: 'Rp. 5.200.000'
            },
            {
                id: 3,
                name: 'Tourista MD 35 Seater Balideva Transport',
                seat: '35',
                image: '/src/assets/images/item-bus-3.png',
                price: 'Rp. 1.750.000'
            },
            {
                id: 4,
                name: 'Toyota Coaster Seater Travelink Trans II',
                seat: '60',
                image: '/src/assets/images/item-bus-2.png',
                price: 'Rp. 4.200.000'
            },
        ]
        return {busList}
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
    .bus-list-btn{
        font-family: "AmsiPro";
        background-color: #3BC5E9;
        color: #fff;
        font-size: 18px;
    }
    .dots-frame{
        position:absolute;
        bottom: -2%;
        left: 6.5%;
        z-index: -10;
    }
    .bus-list{
        max-width:1440px;
        max-height: 820px;
        position: relative;
    }
    .bus-list-card{
        max-width: 354px;
        width: 354px;
        max-height: 468px;
        height: 468px;
    }
    .bl-desc{
        max-width: 95.7%; 
    }
    .bus-list-title h5{
        color: #3BC5E9;
        letter-spacing: .3em;
    }
    h1{
        font-family: "AmsiProSemiBold";
    }
</style>
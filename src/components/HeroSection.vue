<template>
    <section>
        <div class="wrapper relative mx-auto">
            <div class="box-blue w-1/2 xl:w-1/4 absolute -z-10 right-0" style="height: 780px; background-color: #3BC5E9"></div>
            <div class="flex xl:max-w-6xl mx-auto" style="height: 780px;">
                <div class="bus-text w-full h-full flex flex-col justify-center">
                    <h1 class="hero-big-text font-bold xl:text-6xl text-5xl text-stone-900 leading-tight mb-5 xl:w-11/12">Cara Mudah Sewa Bus Pariwisata</h1>
                    <p class="text-sm leading-9 xl:w-9/12 sm:px-20 md:px-0 text-justify">
                        Booking bus untuk segala keperluan berpergian anda seperti perjalanan religi, 
                        kunjungan industri sampai rekreasi bersama orang-orang tercinta
                    </p>
                </div>
                <div class="bus-img w-full h-full flex items-center justify-center">
                    <img class="xl:mt-14 xl:ml-28" :src="'/src/assets/images/bus.png'" alt="" srcset="">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'HeroSection',
}
</script>

<style scoped>
    @media (max-width: 768px) {
        .box-blue{
            /* display: none; */
            /* left:0; */
            right:0;
        }
        .bus-img{
            /* display: none; */
            position: absolute;
            z-index: -2;
            opacity: 0.2;
        }
        .bus-text{
            text-align: center;
        }
        .bus-text p{
            text-align: center;
        }
    }
    .hero-big-text{
        font-family: "AmsiProBlack";
    }
    .wrapper{
        background: url('../assets/images/dots-frame.png');
        max-width: 1440px;
    }
</style>
<template>
    <section>
        <div class="wrapper relative mx-auto">
            <div class="w-1/4 absolute -z-10 right-0" style="height: 780px; background-color: #3BC5E9"></div>
            <div class="flex max-w-6xl mx-auto" style="height: 780px;">
                <div class="w-full h-full flex flex-col justify-center">
                    <h1 class="hero-big-text font-bold text-6xl text-stone-900 leading-tight mb-5 w-11/12">Cara Mudah Sewa Bus Pariwisata</h1>
                    <p class="text-sm leading-9 w-9/12 text-justify">
                        Booking bus untuk segala keperluan berpergian anda seperti perjalanan religi, 
                        kunjungan industri sampai rekreasi bersama orang-orang tercinta
                    </p>
                </div>
                <div class="w-full h-full flex items-center justify-center">
                    <img class="mt-14 ml-28" :src="'/src/assets/images/bus.png'" alt="" srcset="">
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
    .hero-big-text{
        font-family: "AmsiProBlack";
    }
    .wrapper{
        background: url('../assets/images/dots-frame.png');
        max-width: 1440px;
    }
</style>
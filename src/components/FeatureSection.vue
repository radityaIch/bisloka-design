<template>
    <section class="feature mx-auto mb-36">
        <div class="square-background absolute left-0 h-5/6"></div>
        <div class="wrapper relative mx-auto max-w-6xl">
            <div class="container flex flex-col mx-auto">
                <div class="feature-title mb-14 mt-14">
                    <h5 class="text-xs mb-6">TENTANG KAMI</h5>
                    <h1 class="text-5xl">Mengapa Bisloka ?</h1>
                </div>
                <div class="feature-item flex justify-between">
                    <div class="feature-card rounded-xl shadow-lg mb-10 bg-white">
                        <div class="flex flex-col p-12">
                            <div class="mx-auto mb-5">
                                <img class="h-44" :src="`/src/assets/images/walk-illust.svg`">
                            </div>
                            <div><h1 class="fc-title text-2xl mb-5 w-36">Dimana & Kapan Saja</h1></div>
                            <div><p class="fc-desc text-sm mb-3 leading-loose">Website yang responsive dapat dibuka diberbagai gadget anda akan mempermudah penyewaan bus</p></div>
                        </div>
                    </div>
                    <div class="feature-card rounded-xl shadow-lg mb-10 bg-white">
                        <div class="flex flex-col p-12">
                            <div class="mx-auto mb-5">
                                <img class="h-44" :src="`/src/assets/images/cust-illust.svg`">
                            </div>
                            <div><h1 class="fc-title text-2xl mb-5 w-36">Customer Priority</h1></div>
                            <div><p class="fc-desc text-sm mb-3 leading-loose">Customer Service kami akan melayani anda disaat anda mengalami kesulitan di website kami.</p></div>
                        </div>
                    </div>
                    <div class="feature-card rounded-xl shadow-lg mb-10 bg-white">
                        <div class="flex flex-col p-12">
                            <div class="mx-auto mb-5">
                                <img class="h-44" :src="`/src/assets/images/booking-illust.svg`">
                            </div>
                            <div><h1 class="fc-title text-2xl mb-5 w-36">Mudah Booking</h1></div>
                            <div><p class="fc-desc text-sm mb-3 leading-loose">Mudah booking dan konfirmasi ketersediaan unit yang akan digunakan.</p></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="dots-frame">
            <img :src="`./src/assets/images/dots-blue.png`">
        </div>
    </section>
</template>

<script>
export default {
    name: 'FeatureSection'
}
</script>

<style scoped>
    .dots-frame{
        position:absolute;
        right: 2.5%;
        bottom: -8%;
    }
    .feature{
        max-height: 830px;
        max-width:1440px;
        position: relative;
    }
    .feature-card{
        max-width: 354px;
        width: 354px;
    }
    .fc-desc{
        max-width: 95.7%; 
    }
    .feature-title h5{
        letter-spacing: .3em;
        color: #3BC5E9;
    }
    .square-background{
        background-color: #3BC5E9;
        opacity: 0.02;
        width: 95%;
    }
    h1{
        font-family: "AmsiProSemiBold";
    }
</style>
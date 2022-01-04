<template>
    <section class="card-bus relative max-w-6xl mx-auto -mt-24 mb-28 z-20 shadow-xl">
        <div class="container bg-white rounded-xl flex flex-col px-20 py-16">
            <div class="card-title mb-5">
                <h3 class="text-xl mb-1">Hey kamu,</h3>
                <h1 class="text-3xl mb-5">Mau liburan kemana ?</h1>
            </div>
            <form method="post">
                <hr class="card-separator">
                <div class="flex justify-between mt-3 mb-5">
                    <div>
                        <span class="text-sm block mb-2">Departure</span>
                        <label class="card-menu inline">
                            <span class="icon mr-2"><img :src="`/src/assets/images/location.png`"></span>
                            Mau dijemput dimana ? 
                        </label>
                    </div>
                    <div>
                        <span class="text-sm block mb-2">Destination</span>
                        <label class="card-menu inline">
                            <span class="icon mr-2"><img :src="`/src/assets/images/location.png`"></span>
                            Mau dianter kemana ?
                        </label>
                    </div>
                    <div>
                        <span class="text-sm block mb-2">Jenis Bus</span>
                        <label class="card-menu inline">
                            <span class="icon mr-2"><img :src="`/src/assets/images/bus-icon.png`"></span>
                            Pilih jenis bus kamu
                        </label>
                    </div>
                </div>
                <hr class="card-separator mt-2">
                <div class="flex justify-end">
                    <button class="card-btn px-24 py-4 rounded-xl mt-4">Cari Bus</button>
                </div>
            </form>
        </div>
    </section>
</template>

<script>
export default {
    name:'CariBus'
}
</script>

<style scoped>
    .card-btn{
        font-family: "AmsiPro";
        background-color: #3BC5E9;
        color: #fff;
        font-size: 18px;
    }
    .card-bus{
        max-height: 445px;
    }
    .card-menu{
        font-family: "AmsiProSemiBold";
        font-size: 18px;
    }
    .card-separator{
        color: #E0E0E0;
        margin-bottom: 1.5rem;
    }
    .card-title h3{
        font-family: "AmsiPro";
    }
    .card-title h1{
        font-family: "AmsiProBlack";
    }
    .icon{
        max-width: 25px;
        max-height:25px;
    }
    .icon img{
        display: inline;
    }
</style>
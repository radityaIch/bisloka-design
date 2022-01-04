<template>
    <section class="container mx-auto">
        <div class="dots-frame">
            <img :src="`/src/assets/images/dots-blue.png`">
        </div>
        <div class="wrapper max-w-6xl mx-auto h-96 flex justify-between items-center">
            <div class="subscription-text flex flex-col w-7/12">
                <h1 class="text-5xl mb-6 leading-snug">Ayo pesan bus pariwisatamu sekarang !</h1>
                <p class="text-md w-10/12 leading-loose">Booking bus untuk segala keperluan berpergian anda seperti perjalanan religi, kunjungan industri sampai rekreasi bersama orang-orang tercinta</p>
            </div>

            <div class="subscription-form flex flex-col w-4/12">
                <form method="post">
                    <input class="py-5 px-4 w-11/12 mb-5 rounded-xl" type="text" placeholder="Nama Lengkap">
                    <input class="py-5 px-4 w-11/12 mb-5 rounded-xl" type="text" placeholder="Email">
                    <button class="py-5 px-4 w-11/12 rounded-xl bg-blue-300 text-white">Subscribe</button>
                </form>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Subscription'
}
</script>

<style scoped>
    .container{
        position: relative;
        background-color: rgba(59, 198, 233, 0.2);
        max-width: 1440px;
        max-height: 450px;
    }
    .dots-frame{
        position:absolute;
        left: 4%;
        top: 18%;
        z-index: -1;
    }
    h1{
        font-family: "AmsiProBlack";
        font-size: 42px;
    }
    .subscription-form button{
        font-family: "AmsiPro";
        font-size: 18px;
        background-color: #3BC5E9
    }
</style>
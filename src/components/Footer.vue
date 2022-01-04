<template>
    <footer class="container mx-auto">
        <div class="wrapper xl:py-24 py-16 max-w-6xl mx-auto flex xl:flex-row flex-col xl:justify-between items-center">
            <div class="brand w-auto xl:my-0 my-2">© Design by <strong>Innolabs Studio</strong></div>
            <div class="nav mx-auto xl:my-0 my-2">
                <a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300">Booking</a>
				<a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300">List Bus</a>
				<a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300">Blog</a>
				<a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300">Tentang Kami</a>
                <a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300">Sign In</a>
				<a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300">Sign Up</a>
            </div>
            <div class="socials w-auto xl:my-0 my-2">
                <a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300"><img class="inline" :src="`/src/assets/images/ig-icon.svg`" alt=""></a>
                <a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300"><img class="inline" :src="`/src/assets/images/bb-icon.svg`" alt=""></a>
                <a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300"><img class="inline" :src="`/src/assets/images/be-icon.svg`" alt=""></a>
            </div>
        </div>
        <div class="dots-frame">
            <img :src="'/src/assets/images/dots-blue.png'">
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style scoped>
    .container{
        max-width: 1440px;
        max-height: 420px;
        position: relative;
        overflow-y: hidden;
    }
    .dots-frame{
        position:absolute;
        right: 1.5%;
        bottom: -55%;
    }
</style>
<template>
  <header>
      <nav class="bg-transparent fixed w-screen z-50" :class="{change_color_nav: (scrollPosition.value > 50)}">
			<div class="xl:max-w-6xl px-8 mx-auto py-8">
				<div class="flex justify-between">
					<div class="flex space-x-9">
						<div>
							<!-- Website Logo -->
							<a href="#" class="flex items-center py-4">
								<img src="/src/assets/logo.png" alt="Logo">
							</a>
						</div>
						<!-- Primary Navbar items -->
						<div class="hidden lg:flex items-center space-x-1">
							<a href="" class="py-1 px-5 text-blue-400 font-medium ">Booking</a>
							<a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300">List Bus</a>
							<a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300">Blog</a>
							<a href="" class="py-1 px-5 text-gray-500 font-medium hover:text-blue-400 transition duration-300">Tentang Kami</a>
						</div>
					</div>
					<!-- Secondary Navbar items -->
					<div class="hidden lg:flex items-center space-x-3 ">
						<a href="" class="secondary-item py-2 px-5 font-medium text-white rounded hover:bg-blue-400 hover:text-white transition duration-300">Sign In</a>
						<a href="" class="secondary-item py-2 px-5 font-medium text-white hover:text-white border-2 border-white rounded hover:bg-blue-400 transition duration-300">Sign Up</a>
					</div>
				</div>
			</div>
		</nav>
  </header>
</template>

<script>
import { onMounted,reactive } from "vue"
export default {
    name: 'Header',
	setup(){
		const scrollPosition = reactive({
        value: 0,
		})
		function updateScroll() {
			scrollPosition.value = window.scrollY
		}
		onMounted(()=>{
			window.addEventListener('scroll', updateScroll);
		})

		return {scrollPosition}
	}
}
</script>
<style scoped>
	.change_color_nav{
		background-color: #fff;
	}
	.change_color_nav .secondary-item{
		color: #333;
		border: 1px solid #333;
	}
	.change_color_nav .secondary-item:hover{
		color: #fff;
		border: 1px solid #3BC5E9;
	}
</style>
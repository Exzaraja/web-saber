<template>
  <nav>
		<div class="fixed w-[100%] flex items-center justify-between bg-green-600 py-6 text-white shadow-2xl shadow-lime-200">
      

			<!-- Icon -->
		<div class="flex items-center cursor-pointer">
		<span class="text-white text-center mr-2">
		<Icon name="uil:github" class="text-4xl ml-3" />
		</span>

		<h1 class="text-2xl font-semibold">SABER</h1>
		</div>

		<!-- Mobile toggle -->
					<div class="md:hidden">
        <button @click="drawer">
          <svg 
            class=" items-center h-10 w-20 fill-current text-white"
            fill="none" stroke-linecap="round" 
            stroke-linejoin="round" stroke-width="2" 
            viewBox="0 0 24 24" stroke="currentColor">
              <path d="M4 6h16M4 12h16M4 18h16"></path>
          </svg>
        </button>
      </div>

		<!-- Navbar -->
						<div class="hidden md:block ">
        <ul class="flex space-x-10 mr-auto text-xl font-sans">
          <li><NuxtLink to="#">Home</NuxtLink></li>
          <li><a href="./About" class="hover:text-color-secondary ease-in duration-20">About</a></li>
          <li><a href="#" class="hover:text-color-secondary ease-in duration-20">Features</a></li>
          <li><a href="#" class="hover:text-color-secondary ease-in duration-20">FAQ</a></li>
          <li><a href="#" class="hover:text-color-secondary ease-in duration-20">Contact</a></li> 
        </ul>
      </div>

      <div class=" hidden md:block only:flex items-center cursor-pointer">
          <span class="text-white text-center mr-2">
		<Icon name="uil:facebook" class="text-4xl ml-3" />
    <Icon name="uil:instagram" class="text-4xl ml-3" />
    <Icon name="uil:twitter" class="text-4xl ml-3" />
          </span>
        </div>


		<!-- Dark Background Transition -->
						<transition
        enter-class="opacity-0"
        enter-active-class="ease-out transition-medium"
        enter-to-class="opacity-100"
        leave-class="opacity-100"
        leave-active-class="ease-out transition-medium"
        leave-to-class="opacity-0"
      >
        <div @keydown.esc="isOpen = false" v-show="isOpen" class="z-10 fixed inset-0 transition-opacity">
            <div @click="isOpen = false" class="absolute inset-0 bg-black opacity-50" tabindex="0"></div>
        </div>
      </transition>


		<!-- Drawer Menu -->
						<aside class="p-5 transform top-0 left-0 w-64 bg-green-800 fixed h-full overflow-auto ease-in-out transition-all duration-300 z-30" :class="isOpen ? 'translate-x-0' : '-translate-x-full'">
        
        <div class="close">
          <button class="absolute top-0 right-0 mt-4 mr-4" @click=" isOpen = false">
            <svg 
              class="w-6 h-6"
              fill="none" stroke-linecap="round" 
              stroke-linejoin="round" stroke-width="2"
              viewBox="0 0 24 24" stroke="currentColor">
              <path d="M6 18L18 6M6 6l12 12"></path>
            </svg>
          </button>
        </div>


        <ul class="divide-y divide-green-500 font-sans">
          <li><a href="#" @click="isOpen = false" class="my-4 inline-block hover:text-color-secondary ease-in duration-20">Home</a></li>
          <li><a href="#" @click="isOpen = false" class="my-4 inline-block hover:text-color-secondary ease-in duration-20">Services</a></li>
          <li><a href="#" @click="isOpen = false" class="my-4 inline-block hover:text-color-secondary ease-in duration-20">Features</a></li>
          <li><a href="#" @click="isOpen = false" class="my-4 inline-block hover:text-color-secondary ease-in duration-20">FAQ</a></li>
          <li><a href="#" @click="isOpen = false" class="my-4 inline-block hover:text-color-secondary ease-in duration-20">Contact</a></li>

          
          <li><a href="#" @click="isOpen = false" class="my-8 w-full text-center font-semibold inline-block btn">Sign Up</a></li>
        </ul>
      </aside>
	</div>
	</nav>

    <!-- main -->
  <section id="home" class="min-h-screen">
<div class="container py-28 px-5 mx-auto">
<div class="flex items-center z-20 ">
    <div class="text-center mb-20 md:text-left md:w-[800px] md:pr-5">
        <h1 class="title mb-4"> Awesome App for Your Trash.</h1>
        <p class="leading-relaxed mb-5 text-2xl ">Aplikasi yang sangat berguna untuk menjaga lingkungan dengan membuang sampah secara benar agar tidak mencemari lingkungan maka gunakanlah Aplikasi Your Trash Tuker Aja YTTA.</p>
        <p class="leading-relaxed mb-5 text-2xl ">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Libero officia earum minus eius, animi repellendus beatae eum natus nisi incidunt, quibusdam ducimus eveniet suscipit veritatis quo magni. Illo, reprehenderit explicabo!</p>
        <button class="btn text-white">DOWNLOAD APP</button>
    </div>

    <div class="md:w-[400px] hidden md:block ml-auto mr-20">
      <img src="./img/tong-sampah.png" alt="">
    </div>
</div>
</div>
  </section>

  <section id="features"  >
  <div class="text-center justify-between bg-green-500 py-10 h-screen">
    <h4 class="font-bold text-yellow-500 mb-4">Our Features</h4>
    <div class=" container mx-auto items-center p-5 grid lg:grid-cols-3 md:grid-cols-2 gap-12 lg:gap-8 px-4 sm:px-6 lg:px-20">
      <div class="rounded-lg bg-white p-8 shadow-2xl">
        <div>
          <img class="h-16 w-16 rounded-full object-cover" src="./img/tong-sampah.png" alt="">
          <span>Tong Sampah</span>
        </div>
        <div class="nt-2">
          <p class="italic font-thin">Lorem ipsum dolor sit amet consectetur adipisicing elit1. Cum earum recusandae culpa, explicabo ipsum velit!</p>
          <span class="text-sm text-gray-400">Co-Founder of Tong Sampah</span>
        </div>
      </div>

      <div class="rounded-lg bg-white p-8 shadow-2xl">
        <div>
          <img class="h-16 w-16 rounded-full object-cover" src="./img/tong-sampah.png" alt="">
          <span>Tong Sampah</span>
        </div>
        <div class="nt-2">
          <p class="italic font-thin">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum earum recusandae culpa, explicabo ipsum velit!</p>
          <span class="text-sm text-gray-400">Co-Founder of Tong Sampah</span>
        </div>
      </div>

      <div class="rounded-lg bg-white p-8 shadow-2xl">
        <div>
          <img class="h-16 w-16 rounded-full object-cover" src="./img/tong-sampah.png" alt="">
          <span>Tong Sampah</span>
        </div>
        <div class="nt-2">
          <p class="italic font-thin">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum earum recusandae culpa, explicabo ipsum velit!</p>
          <span class="text-sm text-gray-400">Co-Founder of Tong Sampah</span>
        </div>
      </div>
    </div>
  </div>
  </section>

  <section id="features" class="bg-white h-screen">
            <div class=" container mx-auto py-24">
                <div class="text-center m-auto mb-20 md:w-1/2">
                <h4 class="font-bold text-yellow-500 mb-4">Our Features</h4>
                <h1 class="title">Solusi Mempermudah Membuang Sampah Dengan Aplikasi</h1>
                <h1 class="title">Solusi Mempermudah Membuang Sampah Dengan Aplikasi</h1>
                <h1 class="title">Solusi Mempermudah Membuang Sampah Dengan Aplikasi</h1>
                </div>
            </div>
  </section>


<!-- footer -->
<footer id="footer" class=" bg-green-600 py-6 ">
    <div class=" container px-10 mx-auto space-y-5 divide-y divide-white md:-space-x-10 divide-opacity-50">
      <div class="grid grid-cols-12">
        <div class="pb-6 col-span-full md:pb-0 md:col-span-6">
          <a href="#" class="flex justify-center space-x-3 md:justify-start">
            <span class="slef-center text-2xl font-semibold ml-1 mb-10">SABER</span>
          </a>
          <div class="text-center md:block md:text-left">
          <span class="text-white">
		<Icon name="uil:facebook" class="text-4xl" />
    <Icon name="uil:instagram" class="text-4xl ml-3" />
    <Icon name="uil:twitter" class="text-4xl ml-3" />
          </span>
        </div>
        </div>

        <div class="col-span-6 text-center md:text-left md:col-span-3">
          <p class="pb-1 text-lg font-medium">Category</p>
          <ul>
            <li>
              <a href="/about.vue" class="hover:text-color-blob">Link</a>
            </li>
            <li>
              <a href="#" class="hover:text-color-blob">Link</a>
            </li>
            <li>
              <a href="#" class="hover:text-color-blob">Link</a>
            </li>
          </ul>
        </div>
        <div class="col-span-6 text-center md:text-left md:col-span-3">
          <p class="pb-1 text-lg font-medium">Category</p>
          <ul>
            <li>
              <a href="#" class="hover:text-color-blob">Link</a>
            </li>
            <li>
              <a href="#" class="hover:text-color-blob">Link</a>
            </li>
            <li>
              <a href="#" class="hover:text-color-blob">Link</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="grid justify-center pt-4 lg:justify-between">
			<div class="flex flex-col self-center text-sm text-center md:block lg:col-start-1 md:space-x-6">
				<span>©2023 All rights reserved</span>
				<a rel="noopener noreferrer" href="#">
					<span>Privacy policy</span>
				</a>
				<a rel="noopener noreferrer" href="#">
					<span>Terms of service</span>
				</a>
			</div>
		</div>       
    </div>
  </footer>
</template>



<script>

export default {
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    drawer() {
      this.isOpen = !this.isOpen;
    }
  },
  watch: {
    isOpen: {
      immediate: true,
      handler(isOpen) {
        if (process.client) {
          if (isOpen) document.body.style.setProperty("overflow", "hidden");
          else document.body.style.removeProperty("overflow");
        }
      }
    }
  },
  mounted() {
    document.addEventListener("keydown", e => {
      if (e.keyCode == 27 && this.isOpen) this.isOpen = false;
    });
  }
};

</script>
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
          <li><a href="#" class="hover:text-color-secondary ease-in duration-20">Home</a></li>
          <li><a href="#" class="hover:text-color-secondary ease-in duration-20">About</a></li>
          <li><a href="#" class="hover:text-color-secondary ease-in duration-20">Features</a></li>
          <li><a href="#" class="hover:text-color-secondary ease-in duration-20">FAQ</a></li>
          <li><a href="#" class="hover:text-color-secondary ease-in duration-20">Contact</a></li> 
        </ul>
      </div>

      <div class=" hidden md:block only:flex items-center cursor-pointer">
          <span class="text-white text-center mr-2">
		<Icon name="uil:github" class="text-4xl ml-3" />
    <Icon name="uil:github" class="text-4xl ml-3" />
    <Icon name="uil:github" class="text-4xl ml-3" />
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
<section id="about" class="h-screen"></section>
<section id="about" class="h-screen bg-green-500"></section>
<section id="about" class="h-screen"></section>


	<!-- footer -->
<footer id="footer" class=" bg-green-600 py-6 ">
    <div class=" container px-10 mx-auto space-y-5 divide-y divide-white md:-space-x-10 divide-opacity-50">
      <div class="grid grid-cols-12">
        <div class="pb-6 col-span-full md:pb-0 md:col-span-6">
          <a href="#" class="flex justify-center space-x-3 md:justify-start">
            <span class="slef-center text-2xl font-semibold">COMPANY NAME</span>
          </a>
        </div>
        <div class="col-span-6 text-center md:text-left md:col-span-3">
          <p class="pb-1 text-lg font-medium">Category</p>
          <ul>
            <li>
              <a href="" class="hover:text-color-blob">Link</a>
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
        <div class="text-center md:block md:text-left md:col-span-3">
          <span class="text-white">
		<Icon name="uil:github" class="text-4xl ml-3" />
    <Icon name="uil:github" class="text-4xl ml-3" />
    <Icon name="uil:github" class="text-4xl ml-3" />
          </span>
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
<template>
    <div class="bg-white ">
        <Navbar>
            <About></About>
        </Navbar>
    </div>
</template>

<script>
import About from './pages/about.vue';
    import Navbar from "./pages/index.vue";


    export default {
        name: "App",
        components: {
            Navbar,
                About,
        },
    };

</script>
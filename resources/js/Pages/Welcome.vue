<script setup>
import { Head, Link } from '@inertiajs/vue3';
import Hero from '@/Pages/Sections/Hero.vue';
import Services from '@/Pages/Sections/Services.vue';
import Logo from '@/Pages/Sections/Logo.vue';
import Contact from '@/Pages/Sections/Contact.vue';
import Footer from '@/Pages/Sections/Footer.vue';
import Banner from '@/Pages/Sections/Banner.vue';
import About from '@/Pages/Sections/About.vue';
import Gallery from '@/Pages/Sections/Gallery.vue';

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
});
</script>

<template>
    <Head title="Welcome" />

    <Hero />

    <About />

    <Logo />

    <Services />

    <Gallery />

    <Contact />

    <Footer />

    <Banner />

</template>

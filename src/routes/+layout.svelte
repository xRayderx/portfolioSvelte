<script lang="ts">
    import "../app.css";
    import Navbar from '../lib/components/Navbar.svelte';
    import Footer from '../lib/components/Footer.svelte';
</script>

<main class="relative h-screen overflow-hidden bg-gray-300">
    <Navbar />
    <slot />
    <Footer />
</main>

<style lang="scss">
    
</style>
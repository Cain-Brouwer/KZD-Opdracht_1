<script>
    import Hero from '$lib/components/hero/Hero.svelte';
    import Header from '$lib/components/Header.svelte';
    // @ts-ignore
    import Footer from '$lib/components/Footer.svelte';
</script>

<div class="min-h-screen flex flex-col">
    <Hero></Hero>
    <Header></Header>
    <div id="content" class="flex-1 p-4 bg-[url('/Computer.jpg')] bg-cover bg-center min-h-screen"></div>
    <div class="mt-300"></div>
    <Footer></Footer>
</div>


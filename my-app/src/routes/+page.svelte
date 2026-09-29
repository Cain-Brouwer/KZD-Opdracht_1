<script>
    import Hero from '$lib/components/hero.svelte';
    import Header from '$lib/components/header.svelte';
    // @ts-ignore
    import Footer from '$lib/components/footer.svelte';
</script>

<div class="min-h-screen flex flex-col">
    <Hero></Hero>
    <Header></Header>
    <div id="content" class="flex-1 p-4 bg-[url('/Computer.jpg')] bg-cover bg-center min-h-screen"></div>
    <div class="mt-300"></div>
    <Footer></Footer>
</div>


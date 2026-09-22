<script>
    import Hero from '$lib/Components/hero.svelte';
    import Header from '$lib/Components/header.svelte';
    // @ts-ignore
    import Footer from '$lib/Components/footer.svelte';
</script>

<div class="min-h-screen flex flex-col">
    <Hero></Hero>
    <Header></Header>
    <div id="content" class="flex-1 p-4 bg-[url('/Computer.jpg')] bg-cover bg-center"></div>
    <Footer></Footer>
</div>


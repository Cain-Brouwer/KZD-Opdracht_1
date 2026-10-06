<script>
    import Hero from '$lib/components/hero/Hero.svelte';
    // @ts-ignore
    import Header from '$lib/components/header/Header.svelte';
    // @ts-ignore
    import Footer from '$lib/components/footer/Footer.svelte';
    import BgImage from "$lib/components/content/BgImage.svelte";
    import OffersSection from "$lib/components/content/OffersSection.svelte";
</script>

<div class="min-h-screen flex flex-col">
    <Hero></Hero>
    <Header></Header>
    <BgImage></BgImage>
    <OffersSection></OffersSection>
    <Footer></Footer>
</div>


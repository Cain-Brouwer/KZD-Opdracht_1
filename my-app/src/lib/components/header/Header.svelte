<script>
    import Navbar from "$lib/components/header/Navbar.svelte";
    import Logo from "$lib/components/header/Logo.svelte";
    import {onMount} from 'svelte';

    let isScrolled = $state(false);

    let headerClasses = $derived(
        isScrolled
            ? 'sticky top-0 z-10 flex items-center justify-between gap-6 bg-white px-8 pt-4 pb-4 text-black transition-all duration-300 mx-[200px]'
            : 'sticky top-0 z-10 flex items-center justify-between gap-12 bg-white px-16 pt-9 pb-9 text-black transition-all duration-300 mx-auto w-full'
    );

    function handleScroll() {
        isScrolled = window.scrollY > 0;
    }

    onMount(() => {
        window.addEventListener('scroll', handleScroll);
        return () => {
            window.removeEventListener('scroll', handleScroll);
        };
    });

</script>

<div id="header" class="{headerClasses}">
    <Logo/>
    <Navbar/>
</div>

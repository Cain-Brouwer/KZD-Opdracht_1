<script>
    import Navbar from "$lib/components/header/Navbar.svelte";
    import Logo from "$lib/components/header/Logo.svelte";
    import {onMount} from 'svelte';

    let isScrolled = $state(false);

    let headerClasses = $derived(
        isScrolled
            ? `sticky top-0 z-20 flex items-center justify-between gap-3 bg-white px-4 pt-3 pb-3 text-black
            transition-all duration-300 lg:gap-6 lg:px-8 lg:pt-4 lg:pb-4 lg:mx-[200px]`
            : 'sticky top-0 z-20 flex items-center justify-between gap-6 bg-white px-4 pt-5 pb-5 text-black ' +
            'transition-all duration-300 mx-auto w-full lg:gap-12 lg:px-16 lg:pt-9 lg:pb-9'
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

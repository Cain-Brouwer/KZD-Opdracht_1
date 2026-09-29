<script>
    import Navbar from "$lib/components/header/Navbar.svelte";
    import Logo from "$lib/components/header/Logo.svelte";
</script>

<div class="sticky top-0 z-10 flex items-center gap-12 bg-white p-4 pt-9 pb-9 text-black">
    <div class="flex ml-auto">
        <Logo />
    </div>
    <div class="flex ml-auto justify-end mr-80">
    <Navbar />
    </div>
</div>

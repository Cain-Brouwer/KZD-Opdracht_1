<script>
    import { navItems } from "$lib/navItems.js";
</script>
<div class="bg-[#424242] text-white w-full p-6 sm:p-10 flex flex-col sm:flex-row gap-6 sm:gap-0 items-center justify-between text-center sm:text-left">
    <p>Altect © 2021 By Hash Theme. All Rights Reserved</p>
    <div>
        <div class="flex flex-wrap justify-center gap-4 sm:gap-10">
            {#each Object.entries(navItems) as [name, url]}
                <a href="{url}" class="text-white text-sm sm:text-base">
                    {#if name === "Search"}
                        <img src="/search.png" alt="search" class="w-6 h-6">
                    {:else}
                        {name}
                    {/if}
                </a>
            {/each}
        </div>
    </div>
</div>
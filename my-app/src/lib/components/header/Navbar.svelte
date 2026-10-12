<script>
    import { navItems } from '$lib/navItems.js';
</script>

<div class="grid col-span-2 gap-4 mt-4">
    <div class="flex flex-wrap justify-center gap-x-4 gap-y-2 sm:gap-x-6 lg:gap-10">
        {#each Object.entries(navItems) as [name, url]}
            <a href="{url}" class="text-black hover:text-blue-500 text-sm lg:text-base">
                {#if name === "Search"}
                    <img src="/search.png" alt="search" class="w-6 h-6">
                {:else}
                    {name}
                {/if}
            </a>
        {/each}
    </div>
</div>
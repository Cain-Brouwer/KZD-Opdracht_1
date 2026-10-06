<script>
    import { navItems } from "$lib/navItems.js";
</script>
<div class="bg-[#424242] text-white w-full p-10 flex items-center justify-between">
    <p>Altect © 2021 By Hash Theme. All Rights Reserved</p>
    <div>
        <div class="flex justify-center gap-10">
            {#each Object.entries(navItems) as [name, url]}
                <a href="{url}" class="text-white">
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
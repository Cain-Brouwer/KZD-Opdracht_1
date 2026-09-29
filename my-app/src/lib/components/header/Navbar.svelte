<script>
    // @ts-nocheck
    let navItems = {
        "Home": "/",
        "About Us": "/about",
        "Services": "/services",
        "Pages": "/pages",
        "Shop": "/shop",
        "Blog": "blog",
        "Contact Us": "/contact",
        "Search": "/search"
    }
</script>

<div class="grid col-span-2 gap-4 mt-4">
    <div class="flex justify-center gap-10">
        {#each Object.entries(navItems) as [name, url]}
            <a href="{url}" class="text-black hover:text-blue-500">
                {#if name === "Search"}
                    <img src="/search.png" alt="search" class="w-6 h-6">
                {:else}
                    {name}
                {/if}
            </a>
        {/each}
    </div>
</div>
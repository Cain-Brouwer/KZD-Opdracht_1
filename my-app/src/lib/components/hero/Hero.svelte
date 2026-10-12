<script>
    import GetQuoteButton from "$lib/components/hero/GetQuoteButton.svelte";
    import Icons from "./Icons.svelte";
</script>

<div class="grid grid-cols-2 gap-4 bg-[#424242] text-white py-4 px-5 items-center lg:grid-cols-4 lg:gap-8 lg:py-6 lg:px-10">
    <div class="flex items-center col-span-1" id="email">
        <p class="text-left lg:text-right">infoyoursite@mail.com</p>
    </div>
    <div class="flex items-center col-span-1" id="telefoonnummer">
        <p>+31 6 12345678</p>
    </div>
    <div>
        <Icons />
    </div>
    <div>
        <GetQuoteButton />
    </div>
</div>